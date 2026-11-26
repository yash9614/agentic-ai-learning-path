# Agentic AI Learning Path

**Structured path for mastering Agentic AI with LangChain, LangGraph, Agentic RAG, Human-in-the-Loop, Workflows, and MCP.**

This repository is a clean, concept-driven learning path built around your existing course materials. It focuses heavily on **concepts**, **interview questions**, and **must-do projects**.

Original raw dump is left untouched: [D-Downloads-sagenic-ri-btcamp-with-alngjraph-and-raghen](https://github.com/yash9614/D-Downloads-sagenic-ri-btcamp-with-alngjraph-and-raghen)

---

## Related Learning Repos (Your Ecosystem)

| Repo | Focus | Link |
|------|-------|------|
| Generative AI Learning Path | Broad GenAI + LangChain foundations + projects | [generative-ai-learning-path](https://github.com/yash9614/generative-ai-learning-path) |
| Ultimate RAG Bootcamp | Deep RAG techniques, hybrid retrieval, evaluation, agentic RAG | [Ultimate-RAG-Bootcamp](https://github.com/yash9614/Ultimate-RAG-Bootcamp-LangChain-LangGraph-LangSmith) |
| MCP Projects | Hands-on MCP servers, clients, SSE, multi-server | [MCP_PROJECTS_oo3](https://github.com/yash9614/MCP_PROJECTS_oo3) |
| Learning Concepts (makan_m) | Deep notes on agents, RAG, production patterns | [makan_m/learning-concepts](https://github.com/yash9614/makan_m/tree/main/learning-concepts) |
| This repo | Agentic systems, LangGraph, agents, HITL, workflows | You are here |

**Recommended order:** GenAI foundations → RAG depth → Agentic systems (this repo) → MCP integration.

---

## 🚀 Unified Learning Map (Start Here for Cross-Repo Compass)

**[reference/UNIFIED-LEARNING-MAP.md](reference/UNIFIED-LEARNING-MAP.md)** — Single reference synthesizing the highest-signal resources.

**Latest notes:** [reference/NOTE-12-HITL-MULTIAGENT-MAPREDUCE.md](reference/NOTE-12-HITL-MULTIAGENT-MAPREDUCE.md)

**Moved high-signal concepts:** [reference/concepts/](reference/concepts/)

---

## Learning Path Overview

| Stage | Folder | Focus | Priority |
|-------|--------|-------|----------|
| 1 | `01-foundations-agents` | Agents vs Agentic AI, core concepts | High |
| 2 | `02-langgraph-basics` | State graphs, nodes, edges, reducers, subgraphs, memory, commands | High |
| 3 | `03-react-and-tool-calling` | ReAct agents, multi-tool chatbots, supervisor, handoffs, deep agents | Critical |
| 4 | `04-agentic-rag` | Corrective, Adaptive, Agentic RAG loops + production retrieval | Critical |
| 5 | `05-human-in-the-loop` | HITL patterns, parallel interrupts, tool interrupts, durable checkpoints | High |
| 6 | `06-workflows-and-routing` | Workflows, routers, subgraphs, dynamic nodes, Send/map-reduce | High |
| 7 | `07-mcp-integration` | LangGraph + MCP, tool servers | High |
| 8 | `08-projects-and-interview` | Must-do projects + interview Q bank | Critical |

Work the folders in order. Each has a detailed README with concepts, what to study, interview questions, and links back to source notebooks.

**Updated with Telusko (through 23 Nov 2026):** Advance LangGraph + Agents in LangGraph 21-11 (streaming modes, human approval, plan-and-execute, multi-agent supervisor, handoffs, orchestrator-workers, deep agents) + Agentic AI Final Project 22-11 (Meal Planner Kitchen Team: multi-agent + RAG with pgvector + MCP + Postgres short/long-term memory + FastAPI + frontend).

**External progressive tutorials:** See [reference/EXTERNAL-LANGGRAPH-TUTORIALS.md](reference/EXTERNAL-LANGGRAPH-TUTORIALS.md).

**RAG resources:** See [reference/EXTERNAL-RAG-RESOURCES.md](reference/EXTERNAL-RAG-RESOURCES.md).

**Scanned external sources:** See [reference/EXTERNAL-SCANNED-RESOURCES.md](reference/EXTERNAL-SCANNED-RESOURCES.md).

**entbappy projects:** See [reference/ENTBAPPY-RESOURCES.md](reference/ENTBAPPY-RESOURCES.md) (supervisor + MCP + guardrails + HITL, enterprise agentic RAG with private KB + web fallback).

**Starred & forked:** See [reference/STARRED-AND-FORKED-RESOURCES.md](reference/STARRED-AND-FORKED-RESOURCES.md).

**Session map:** See [reference/TELUSKO-SESSION-MAP.md](reference/TELUSKO-SESSION-MAP.md).

---

## Must-Do Projects (Priority Order)

These give the highest ROI for interviews and real systems. Complete them.

1. **Simple LangGraph State Graph** — Understand nodes, edges, state.
2. **Parallel + Reducer Graph** — Fan-out that merges via reducer.
3. **ReAct Tool-Calling Agent** — Wikipedia / Arxiv / search tools with conditional routing.
4. **Agentic / Corrective RAG Loop** — Grade documents, rewrite query, retrieve again (prefer hybrid + rerank).
5. **Human-in-the-Loop Approval Agent** — Interrupt for sensitive actions (including parallel and tool-level), durable with SqliteSaver.
6. **Subgraph Workflow** — Parent that embeds or invokes a subgraph.
7. **Multi-Tool Chatbot with Routing** — Route between vector store, web search, SQL.
8. **MCP-Enabled Agent** — Expose tools via MCP and call them from LangGraph.
9. **Telusko Final Project — Meal Planner Kitchen Team** — Multi-agent supervisor + RAG + MCP + Postgres memory + FastAPI.
10. **End-to-End Workflow** (optional) — News agent, blog generator, or multi-agent research with memory and streaming.

Details and source file pointers are in `08-projects-and-interview/MUST-DO-PROJECTS.md`.

---

## Key Concepts You Must Master

- Agent vs Agentic AI
- ReAct (Reason + Act) pattern
- LangGraph StateGraph, nodes, edges, conditional edges, parallel, loops
- Reducers for parallel writes to the same field
- Subgraphs (attachment styles, state mapping, memory)
- Tool calling / function calling (including tools inside graphs)
- State management (TypedDict, dataclass, Pydantic)
- Agentic RAG loops (grade → rewrite → retrieve)
- Production retrieval inside agents (hybrid + RRF, reranking, metadata filters, citations, evaluation)
- Human-in-the-loop (interrupts, parallel interrupts, checkpoints, resume)
- Commands, Send/map-reduce, dynamic nodes
- Routing and multi-agent patterns (supervisor, handoffs, orchestrator-worker, evaluator-optimizer, deep agents)
- Memory and persistence (InMemorySaver, SqliteSaver, Postgres store)
- MCP (Model Context Protocol) as tool interface

---

## Setup (uv)

This repo is designed to work with [uv](https://docs.astral.sh/uv/) for fast, reliable dependency management.

```bash
# Install uv if you don't have it: https://docs.astral.sh/uv/getting-started/installation/

# From the repo root
uv sync
cp .env.example .env   # then fill in your API keys

# Run notebooks or scripts
uv run jupyter lab
# or
uv run python some_script.py
```

**Windows PowerShell:**
```powershell
uv sync
copy .env.example .env
uv run jupyter lab
```

Use `.env` for API keys. Never hardcode them.

Add packages as needed with `uv add package-name`.

---

## How to Use This Repo

1. Read each module README carefully (concepts + interview questions).
2. Open the linked notebooks from the original dump and run them.
3. Complete the Must-Do Projects.
4. Practice the interview questions out loud.
5. Cross-reference the RAG and GenAI repos for deeper foundations.
6. For the latest Telusko code, see the course repo session folders and the [session map](reference/TELUSKO-SESSION-MAP.md).
7. Supplement with the progressive tutorials in [reference/EXTERNAL-LANGGRAPH-TUTORIALS.md](reference/EXTERNAL-LANGGRAPH-TUTORIALS.md).
8. Check [reference/STARRED-AND-FORKED-RESOURCES.md](reference/STARRED-AND-FORKED-RESOURCES.md) and [reference/EXTERNAL-SCANNED-RESOURCES.md](reference/EXTERNAL-SCANNED-RESOURCES.md) for additional project ideas and interview banks.
9. Use the [Unified Learning Map](reference/UNIFIED-LEARNING-MAP.md) as your cross-repo compass.
10. Review the latest session notes: [NOTE-12-HITL-MULTIAGENT-MAPREDUCE.md](reference/NOTE-12-HITL-MULTIAGENT-MAPREDUCE.md).
11. Read the moved high-signal concepts in [reference/concepts/](reference/concepts/).
12. Study entbappy multi-agent and enterprise RAG patterns: [reference/ENTBAPPY-RESOURCES.md](reference/ENTBAPPY-RESOURCES.md).

Start with `01-foundations-agents/README.md`.

Happy building agents!
