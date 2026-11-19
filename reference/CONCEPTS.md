# Concept Glossary — Agentic AI

| Term | Meaning |
|------|---------|
| **Agent** | LLM + tools + decision loop (brain + hands) |
| **ReAct** | Reason → Act → Observe loop |
| **LangGraph** | Explicit state graph (nodes, edges, conditional routing, checkpointers) |
| **State** | Shared data structure nodes read/write (usually one Pydantic model) |
| **Node** | Function that returns a partial state update |
| **Conditional Edge** | Router that decides next node |
| **Reducer** | Function that merges parallel writes to the same state field (`Annotated[type, reducer]`) |
| **Subgraph** | A graph attached inside another (as a node or via invoke). State mapping depends on attachment style. |
| **Checkpointer** | Persists state for memory and HITL (`InMemorySaver`, `SqliteSaver`). One checkpoint per step. |
| **Command** | `Command(update=..., goto=..., resume=...)` for explicit control and resuming interrupts |
| **Send** | Dynamic fan-out (map-reduce style) to multiple nodes |
| **Dynamic nodes/edges** | Nodes or conditional edges created at runtime based on state |
| **Parallel interrupts** | Multiple nodes interrupt in the same step; answered by interrupt id |
| **CrewAI** | Role-based multi-agent (Agent + Task + Crew + Process) |
| **Deep Agents** | Opinionated harness (planning, filesystem, subagents) on LangChain + LangGraph |
| **Agentic RAG** | Agent controls retrieval (decide, decompose, re-retrieve) |
| **CRAG** | Grades retrieval and corrects (rewrite / web search) |
| **Self-RAG** | Model decides whether to retrieve and critiques its own answer |
| **MCP** | Standard protocol for tool servers |
| **HITL** | Human-in-the-loop via interrupts (can live in nodes or tools) |
| **Harness** | Guardrails, step limits, validation, observability around the model |

## Stack Layers

- LangGraph = runtime
- LangChain = framework
- Deep Agents = harness
- CrewAI = role-based team abstraction

Deeper notes: [makan_m/learning-concepts](https://github.com/yash9614/makan_m/tree/main/learning-concepts) (modules 10–20)
