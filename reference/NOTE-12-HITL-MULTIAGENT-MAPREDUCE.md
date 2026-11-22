# Note 12 — HITL, Multi-Agent Architectures, Map-Reduce & Conditional Routing

Clean transcription + expanded notes from the handwritten session notes (Note 12).

**Topics covered:**
- Human-in-the-Loop (HITL) with `interrupt` and `Command(resume=...)`
- Multi-Agent Architectures — Map-Reduce pattern using the **Send API**
- Conditional Routing with `Command` (vs classic conditional edges)
- Supervisor pattern with sub-agents / subgraphs

These map directly to **Stage 05 (HITL)** and **Stage 06 (Workflows & Routing)** in this learning path, and to the Advance LangGraph sessions in the Telusko course.

---

## 1. Human in the Loop (HITL)

### Interrupt
Pauses the graph and waits for human approval or rejection.

```python
from langgraph.types import interrupt

def human_approval_node(state):
    # Pause execution and wait for human input
    decision = interrupt({
        "question": "Do you approve this action?",
        "context": state["proposed_action"]
    })
    return {"approved": decision["approved"]}
```

### Command(Resume)
Resumes graph execution after the human provides input.

```python
from langgraph.types import Command

# After human responds:
result = graph.invoke(
    Command(resume={"approved": True}),
    config={"configurable": {"thread_id": "session-1"}}
)
```

**Key points from notes:**
- `interrupt(...)` → pause the graph and wait for human approval/rejection
- `Command(resume=...)` → resumption of the graph execution

**Related resources:**
- Stage `05-human-in-the-loop`
- [sourangshupal 05_human_in_the_loop_streaming.ipynb](https://github.com/sourangshupal/langraph-tutorials/blob/main/05_human_in_the_loop_streaming.ipynb)
- Telusko Types of Graphs Part-2/3/4 (HITL programs 16–23)

---

## 2. Multi-Agent Architectures — Map-Reduce Pattern

**Design Pattern: Map-Reduce using the Send API**

Example: 100 documents → Summarize them

### Stage 1: Map
Divide 100 docs into smaller independent tasks.

```
Worker 1 → 10 docs
Worker 2 → 10 docs
...
Worker 10 → 10 docs
```

All workers can work **independently & in parallel**.

### Stage 2: Reduce
- Collect all 100 summaries
- Combine all results into a final output

### How it looks in LangGraph (Send API)

```python
from langgraph.types import Send

def map_node(state):
    # Dynamically fan-out
    return [
        Send("worker", {"docs": batch})
        for batch in state["document_batches"]
    ]

def worker_node(state):
    # Process one batch
    summary = summarize(state["docs"])
    return {"summaries": [summary]}

def reduce_node(state):
    # Combine all summaries
    final = "\n".join(state["summaries"])
    return {"final_summary": final}
```

**Diagrams from notes:**
- Fan-out from a Task node to multiple workers (D1, D2, D3 → O1, O2, O3) then Fan-In (FO)
- Main Node fanning out to Node 1/2/3/4 → converging into Node 5 → FO

**Related resources:**
- Stage `06-workflows-and-routing`
- Telusko Advance LangGraph programs with `Send` (e.g. `38_send_map_reduce.py`)
- [sourangshupal app/01_send_basic.py](https://github.com/sourangshupal/langraph-tutorials/blob/main/app/01_send_basic.py) and other Send demos

---

## 3. Conditional Routing in LangGraph

Two ways to route:

1. **Classic conditional edge** (`add_conditional_edges`)
2. **Command** (more explicit and flexible)

### Using Command for routing

```python
from langgraph.types import Command
from typing import Literal

def supervisor_node(state) -> Command[Literal["web_agent", "code_agent"]]:
    task = state["task"].lower()
    
    if "search" in task or "web" in task:
        return Command(goto="web_agent")
    else:
        return Command(goto="code_agent")
```

**From the notes:**
```python
if task == "...":
    Command(goto="web_agent")
else:
    Command(goto="code_agent")
```

### Supervisor Pattern

```
Supervisor
   ↓
Evaluate Condition
   ↓              ↓
Web Agent       Code Agent
(Node 1)        (Node 2)
Sub-agent / Subgraph
```

The supervisor decides which specialized sub-agent (or subgraph) should handle the task.

**Related resources:**
- Stage `06-workflows-and-routing`
- [sourangshupal 09_multi_agent_systems.ipynb](https://github.com/sourangshupal/langraph-tutorials/blob/main/09_multi_agent_systems.ipynb)
- [sourangshupal app/07_multiagent.py](https://github.com/sourangshupal/langraph-tutorials/blob/main/app/07_multiagent.py)
- Telusko Advance LangGraph (Command + subgraphs)

---

## 4. Quick Reference

| Concept | What the notes say | LangGraph primitive |
|---------|--------------------|---------------------|
| HITL Pause | Interrupt: Pause the graph and wait for human approval/rejection | `interrupt(...)` |
| HITL Resume | Command(Resume): Resumption of the graph execution | `Command(resume=...)` |
| Map-Reduce | Divide work → parallel workers → combine results | `Send` API |
| Routing | Conditional Routing with Command | `Command(goto=...)` |
| Supervisor | Supervisor → Evaluate → Web/Code sub-agents | Supervisor node + subgraphs |

---

## Recommended Next Steps

1. Run the HITL examples in Stage 05 and sourangshupal notebook 05.
2. Implement a simple Map-Reduce with `Send` (summarize a list of texts).
3. Build a Supervisor that routes between two specialist subgraphs using `Command`.
4. Combine HITL inside a multi-agent flow (human approval before a sensitive tool call).

These notes align perfectly with the must-do projects around HITL, subgraphs, and multi-agent systems in this learning path.

**Source:** Handwritten notes (Note 12) uploaded 22 Nov 2026.
