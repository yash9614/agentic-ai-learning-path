# 🚀 Agentic AI Unified Learning Map

> **Single reference** synthesizing the highest-signal public resources for mastering LangGraph, Agentic RAG, MCP, HITL, Multi-Agent Systems, and production patterns.  
> Built from Telusko’s course code, sourangshupal’s progressive tutorials, sunnysavita10’s Full-Stack GenAI Bootcamp, and this learning path’s structure.

**Use this as the cross-repo compass.** Pair it with the stage folders in this repo and the [Telusko Session Map](TELUSKO-SESSION-MAP.md).

---

## 🎯 Core Overlap — What Every High-Quality Resource Emphasizes

These are the patterns that appear consistently across Telusko Advance LangGraph, sourangshupal’s 10 notebooks, sunnysavita Classes 40–59, and this path. Master them first.

| Priority | Concept | Why It Matters | Best Coverage |
|----------|---------|----------------|---------------|
| ⭐⭐⭐⭐⭐ | **StateGraph + Reducers** | Foundation of every real workflow | Telusko Advance + sourangshupal 01–02 + this repo Stage 02 |
| ⭐⭐⭐⭐⭐ | **Tool Calling + ReAct** | Agents that actually do things | Telusko Tools + sourangshupal 03 + Stage 03 |
| ⭐⭐⭐⭐⭐ | **Memory & Checkpointers** | Conversations that remember | Both + sunnysavita Classes 43–45 + Stage 02/05 |
| ⭐⭐⭐⭐⭐ | **Human-in-the-Loop (HITL)** | Safe, controllable agents | Telusko 16–23 + sourangshupal 05 + Stage 05 |
| ⭐⭐⭐⭐⭐ | **Subgraphs + Multi-Agent** | Composition & specialization | Telusko 24–34 + sourangshupal 06 & 09 + Stage 06 |
| ⭐⭐⭐⭐ | **Command & Send** | Advanced control flow & map-reduce | Telusko Advance + sourangshupal 08 + `app/` demos |
| ⭐⭐⭐⭐ | **Agentic / Corrective RAG** | Retrieval that can self-correct | Telusko RAG modules + Stage 04 + Ultimate RAG Bootcamp |
| ⭐⭐⭐⭐ | **MCP as Tool Interface** | Standardized, composable tools | Telusko MCP + [mcp-learning-path](https://github.com/yash9614/mcp-learning-path) + Stage 07 |
| ⭐⭐⭐ | **Observability & Evaluation** | Production readiness | sourangshupal 10 + sunnysavita Classes 58–59 (DeepEval) |

---

## 📚 Resource Map & How to Use Them With This Path

### Primary Sources

| Resource | Style | Strengths | How to Pair With This Repo |
|----------|-------|-----------|----------------------------|
| [telusko-aliens/agentic-ai-engineering-with-python](https://github.com/telusko-aliens/agentic-ai-engineering-with-python) | Session-wise Python scripts (Aug–Nov 2026) | Real projects (Secure RAG, Support App + MCP), deep Advance LangGraph (reducers, parallel interrupts, Command, Send, subgraph memory) | See [TELUSKO-SESSION-MAP.md](TELUSKO-SESSION-MAP.md) — maps every session to stages 01–08 |
| [sourangshupal/langraph-tutorials](https://github.com/sourangshupal/langraph-tutorials) | Clean progressive notebooks (LangGraph 1.1.9) | Excellent structure, modern features, production patterns, multi-agent, testing & observability. Also has `app/` pure Python demos | Best complement to Stages 02, 03, 05, 06. See [EXTERNAL-LANGGRAPH-TUTORIALS.md](EXTERNAL-LANGGRAPH-TUTORIALS.md) |
| [sunnysavita10/Full-Stack-GenAI-Bootcamp-1.0](https://github.com/sunnysavita10/Full-Stack-GenAI-Bootcamp-1.0) | 59-class bootcamp (Mar–Nov 2026) | Deep foundations (transformers → fine-tuning → RAG) + later agentic modules + interview Q bank + DeepEval | Classes 40–59 align with Stages 01–06 + evaluation. Strong interview material in `GenAI-Interview-Questions/` |
| This repo (`agentic-ai-learning-path`) | Structured stages + concepts + interview Qs + must-do projects | Distillation + cross-references + interview focus | Work stages in order; use this map as the external compass |

### Related Ecosystem (Your Other Repos)

- [generative-ai-learning-path](https://github.com/yash9614/generative-ai-learning-path) — broader foundations
- [Ultimate-RAG-Bootcamp-LangChain-LangGraph-LangSmith](https://github.com/yash9614/Ultimate-RAG-Bootcamp-LangChain-LangGraph-LangSmith) — production RAG depth
- [mcp-learning-path](https://github.com/yash9614/mcp-learning-path) — focused MCP curriculum

**Recommended overall order:** GenAI foundations → RAG depth → Agentic systems (this repo + Telusko + sourangshupal) → MCP integration.

---

## 🗺️ Recommended Unified Path (Aligned to This Repo’s Stages)

| Phase | Duration | Focus | Primary Resources | This Repo Stage |
|-------|----------|-------|-------------------|-----------------|
| **1. Foundations** | 1–2 weeks | LLM basics, Pydantic, basic RAG intuition | Telusko early sessions or sunnysavita Classes 1–16 | `01-foundations-agents` |
| **2. LangGraph Core** | 2–3 weeks | StateGraph, conditional edges, parallel + reducers, tools, memory, HITL, subgraphs | sourangshupal 01–06 + Telusko LangGraph sessions | `02` + `03` + `05` |
| **3. Agentic RAG** | 1–2 weeks | Corrective/Adaptive loops, hybrid + rerank, evaluation | Telusko RAG modules + Ultimate RAG Bootcamp | `04-agentic-rag` |
| **4. Advanced Control + MCP** | 1–2 weeks | Command, Send, dynamic nodes, MCP servers/clients/adapters | Telusko Advance + sourangshupal 08 + MCP path | `06` + `07-mcp-integration` |
| **5. Multi-Agent + Production** | 1–2 weeks | Orchestrator-worker, guardrails, observability, streaming, durable checkpoints | sourangshupal 07/09/10 + sunnysavita Classes 49–59 | `06` + `08-projects-and-interview` |

---

## 🏆 Must-Do Projects (Cross-Repo Priority)

These give the highest interview and production ROI. Complete them in roughly this order. Full details live in [`08-projects-and-interview/MUST-DO-PROJECTS.md`](../08-projects-and-interview/MUST-DO-PROJECTS.md).

| # | Project | Skills | Primary Sources |
|---|---------|--------|-----------------|
| 1 | Simple StateGraph with conditional edge | Core LangGraph | sourangshupal 01–02, Telusko early |
| 2 | Parallel + Reducer graph | Fan-out / merge | Telusko reducers, sourangshupal 06 |
| 3 | ReAct multi-tool agent | Tool calling + routing | Telusko tools, sourangshupal 03 |
| 4 | Agentic/Corrective RAG loop | Self-correcting retrieval | Telusko RAG, Stage 04, Ultimate RAG |
| 5 | HITL approval agent (durable) | Interrupts + SqliteSaver | Telusko 16–23, sourangshupal 05 |
| 6 | Subgraph workflow | Composition | Telusko 24–30, sourangshupal 06 |
| 7 | MCP-powered agent | Standardized tools | Telusko MCP, mcp-learning-path |
| 8 | Multi-agent research/support system | Orchestration | sourangshupal 09, Telusko projects |
| 9 | Production RAG with eval + hybrid | Real retrieval quality | Telusko Secure RAG, sunnysavita RAG |
| 10 | Full support app (MCP + HITL + memory) | End-to-end | Telusko Support App with MCP |

---

## 🔑 Concept Cheat Sheet

| Term | One-Liner |
|------|-----------|
| **State** | Shared TypedDict / Pydantic model that flows through nodes |
| **Reducer** | Merges parallel writes to the same field (`Annotated[list, operator.add]`) |
| **Command** | `Command(update=..., goto=..., resume=...)` — explicit control + interrupt resume |
| **Send** | Dynamic fan-out (map-reduce style) |
| **Checkpointer** | Persists state for memory + HITL (`InMemorySaver`, `SqliteSaver`) |
| **HITL** | Interrupt → human input → resume (can be in nodes or tools) |
| **Agentic RAG** | Agent decides whether/how to retrieve, can rewrite & retry |
| **CRAG / Self-RAG** | Grade retrieval and correct, or model decides whether to retrieve |
| **MCP** | Standard protocol for exposing tools as servers (stdio / SSE / Streamable HTTP) |
| **Subgraph** | Graph used as a node or invoked inside another graph (state mapping matters) |

Full glossary: [CONCEPTS.md](CONCEPTS.md)

---

## 🛠️ Practical Setup (Common Pattern)

```bash
uv sync
cp .env.example .env   # add OPENAI_API_KEY (and others as needed)
uv run python script.py
# or
uv run jupyter lab
```

- Prefer `uv` + `pyproject.toml`.
- Never commit `.env`.
- Start with `gpt-4o-mini` for cost control.
- Turn on LangSmith tracing early.
- For durable HITL: use `SqliteSaver` (or similar) instead of pure in-memory.

---

## 📎 Quick Links

- [Telusko Session Map](TELUSKO-SESSION-MAP.md)
- [External LangGraph Tutorials](EXTERNAL-LANGGRAPH-TUTORIALS.md)
- [5-Star Must-Dos](5-STAR-MUST-DOS.md)
- [Concepts Glossary](CONCEPTS.md)
- [Must-Do Projects](../08-projects-and-interview/MUST-DO-PROJECTS.md)
- [MCP Learning Path](https://github.com/yash9614/mcp-learning-path)

---

**Last updated:** 21 November 2026  
**Purpose:** Cross-repo compass for this learning path. Keep it updated when new high-signal resources appear.

Happy building agents! 🤖
