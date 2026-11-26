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

## 4. Agentic / Corrective RAG (with Production Retrieval)
**Goal:** Retrieval that can self-correct.  
**Source:** Original agentic/corrective RAG notebooks + production RAG guide  
**Deliverable:** Grade → rewrite → re-retrieve loop.  
**Stronger version:** Use hybrid search (dense + BM25 + RRF) and cross-encoder reranking inside the retrieval step. Measure with a small evaluation set (Hit@K + groundedness score).

See the production patterns in the Generative AI learning path: [PRODUCTION-RAG-GUIDE.md](https://github.com/yash9614/generative-ai-learning-path/blob/main/03-RAG-Systems/PRODUCTION-RAG-GUIDE.md).

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

## 10. Full-Stack Hybrid Agent (Project Streak reference)
**Goal:** End-to-end practical application with dual paths.  
**Source:** [yash9614/project_streak_](https://github.com/yash9614/project_streak_) — especially `projects/00-travel-planning-agent`  
**Deliverable:** Run the Travel Planning Agent (Streamlit direct + FastAPI + MCP). Add one new tool or knowledge document. Understand the dual-path design.  
**Most important skill demonstrated:** Hybrid agents that combine structured tools + RAG + MCP as a reusable interface.

## 11. Telusko Final Project — Meal Planner Kitchen Team (High priority)
**Goal:** Multi-agent supervisor + RAG + MCP + short/long-term memory in one system.  
**Source:** `Agentic AI Final Project 22-11-2026/Project`  
**Deliverable:** Run the full stack (Docker Postgres + pgvector, MCP server, CLI or FastAPI frontend). Understand how the Head Chef supervisor routes to recipe (RAG), nutrition (MCP), and grocery (store) agents, and how short-term (checkpointer) and long-term (store) memory are isolated by user.  
**Key skills:** Multi-agent supervisor, RAG with pgvector, MCP tools, Postgres-backed memory, FastAPI + frontend, message trimming.

---

**Interview tip:** Be ready to explain the design decisions, failure modes, and how you would productionize each project (observability, evaluation, cost control, guardrails, durable checkpoints, hybrid retrieval, reranking).
