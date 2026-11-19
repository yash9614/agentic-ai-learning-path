# Must-Do Projects

Complete these in order. They map directly to common interview expectations and the Telusko course progression.

## 1. Simple State Graph
**Goal:** Master LangGraph fundamentals.  
**Source:** Telusko programs 1–6 or `1-simplegraph.ipynb`  
**Deliverable:** A working graph with at least one conditional edge.

## 2. Parallel + Reducer Graph
**Goal:** Understand parallel nodes and merging.  
**Source:** Telusko programs 7, 11–15  
**Deliverable:** Fan-out to 2–3 nodes that write the same field via a reducer.

## 3. ReAct Tool-Calling Agent
**Goal:** Production-style agent with tools.  
**Source:** Telusko agents project (`2_agents_with_tools.py`, `3_agent_with_multiple_tools.py`) or original ReAct notebooks  
**Deliverable:** Agent that uses 2+ tools and stops correctly.

## 4. Agentic / Corrective RAG
**Goal:** Retrieval that can self-correct.  
**Source:** Original agentic/corrective RAG notebooks  
**Deliverable:** Grade → rewrite → re-retrieve loop.

## 5. Human-in-the-Loop Agent
**Goal:** Safe agents.  
**Source:** Telusko programs 16–23 (including parallel interrupts and tool interrupts)  
**Deliverable:** Approval gate on a sensitive action, preferably with SqliteSaver so it survives restart.

## 6. Subgraph Workflow
**Goal:** Composition.  
**Source:** Telusko programs 24–30  
**Deliverable:** Parent graph that embeds or invokes a subgraph (optionally with HITL inside the subgraph).

## 7. Routing Agent / Multi-Source
**Goal:** Intelligent tool/source selection.  
**Deliverable:** Router between vector DB and web search.

## 8. MCP-Powered Agent
**Goal:** Modern tool architecture.  
**Sources:** MCP session folders + [MCP_PROJECTS_oo3](https://github.com/yash9614/MCP_PROJECTS_oo3)  
**Deliverable:** LangGraph agent calling tools via MCP.

## 9. Agents with Memory & Streaming (Optional but strong)
**Goal:** Production feel.  
**Source:** Telusko `agents` project (programs 6–9) + memory programs 31–34  
**Deliverable:** Agent with checkpointer memory and streaming output.

---

**Interview tip:** Be ready to explain the design decisions, failure modes, and how you would productionize each project (observability, evaluation, cost control, guardrails, durable checkpoints).
