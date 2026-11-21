# 🚀 Agentic AI Unified Learning Map

> **Single reference** synthesizing the highest-signal public resources for mastering LangGraph, Agentic RAG, MCP, HITL, Multi-Agent Systems, and production patterns.  
> Built from Telusko’s course code, sourangshupal’s progressive tutorials, sunnysavita10’s Full-Stack GenAI Bootcamp, and this learning path’s structure.

**Use this as the cross-repo compass.** Pair it with the stage folders in this repo and the [Telusko Session Map](TELUSKO-SESSION-MAP.md).

---

## 🎯 Core Overlap — What Every High-Quality Resource Emphasizes

These are the patterns that appear consistently across Telusko Advance LangGraph, sourangshupal’s 10 notebooks, sunnysavita Classes 40–59, and this path. Master them first.

| Priority | Concept | Why It Matters | Best Coverage (Direct Links) |
|----------|---------|----------------|------------------------------|
| ⭐⭐⭐⭐⭐ | **StateGraph + Reducers** | Foundation of every real workflow | [Telusko Advance LangGraph 14-Nov](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Advance%20LangGraph%2014-11-2026) · [sourangshupal 01](https://github.com/sourangshupal/langraph-tutorials/blob/main/01_introduction_to_langgraph.ipynb) + [02](https://github.com/sourangshupal/langraph-tutorials/blob/main/02_conditional_routing.ipynb) · Stage 02 |
| ⭐⭐⭐⭐⭐ | **Tool Calling + ReAct** | Agents that actually do things | [Telusko Tools](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/LangChain%20Tools%20and%20Agents%2030-08-2026) + [Tool Calling Part-2](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Tool%20Calling%20(Part-2)%20-%2005-09-2026) · [sourangshupal 03](https://github.com/sourangshupal/langraph-tutorials/blob/main/03_tool_integration_openai.ipynb) · Stage 03 |
| ⭐⭐⭐⭐⭐ | **Memory & Checkpointers** | Conversations that remember | [sourangshupal 04](https://github.com/sourangshupal/langraph-tutorials/blob/main/04_state_persistence_and_memory.ipynb) · Telusko Advance memory programs · sunnysavita Classes 43–45 · Stage 02/05 |
| ⭐⭐⭐⭐⭐ | **Human-in-the-Loop (HITL)** | Safe, controllable agents | [Telusko Types of Graphs Part-2/3/4](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Types%20of%20Graphs%20(Part%20-%202)%2031-10-2026) · [sourangshupal 05](https://github.com/sourangshupal/langraph-tutorials/blob/main/05_human_in_the_loop_streaming.ipynb) · Stage 05 |
| ⭐⭐⭐⭐⭐ | **Subgraphs + Multi-Agent** | Composition & specialization | [Telusko Advance subgraphs](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Advance%20LangGraph%2014-11-2026) · [sourangshupal 06](https://github.com/sourangshupal/langraph-tutorials/blob/main/06_parallel_execution_subgraphs.ipynb) + [09](https://github.com/sourangshupal/langraph-tutorials/blob/main/09_multi_agent_systems.ipynb) · Stage 06 |
| ⭐⭐⭐⭐ | **Command & Send** | Advanced control flow & map-reduce | Telusko Advance (programs 35–40) · [sourangshupal 08](https://github.com/sourangshupal/langraph-tutorials/blob/main/08_command_functional_api_longterm_memory.ipynb) · [app/ demos](https://github.com/sourangshupal/langraph-tutorials/tree/main/app) |
| ⭐⭐⭐⭐ | **Agentic / Corrective RAG** | Retrieval that can self-correct | [Telusko RAG Fundamentals](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/RAG%20Fundamentals%20and%20Production%20Techniques%2027-09-2026) + [Complete RAG](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Building%20a%20Complete%20RAG%20Application%2004-10-2026) · Stage 04 · Ultimate RAG Bootcamp |
| ⭐⭐⭐⭐ | **MCP as Tool Interface** | Standardized, composable tools | [Telusko MCP Part-2](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/MCP%20(Part%20-%202)%2013-09-2026) · [Support App with MCP](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Building%20a%20Support%20App%20with%20MCP%2011-10-2026) · [mcp-learning-path](https://github.com/yash9614/mcp-learning-path) · Stage 07 |
| ⭐⭐⭐ | **Observability & Evaluation** | Production readiness | [sourangshupal 10](https://github.com/sourangshupal/langraph-tutorials/blob/main/10_testing_observability_platform.ipynb) · sunnysavita Classes 58–59 (DeepEval) |

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

| Phase | Duration | Focus | Primary Resources (Direct) | This Repo Stage |
|-------|----------|-------|----------------------------|-----------------|
| **1. Foundations** | 1–2 weeks | LLM basics, Pydantic, basic RAG intuition | [Telusko Calling Your First LLM](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Calling%20Your%20First%20LLM) · [Data Modeling with Pydantic](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Data%20Modeling%20with%20Pydantic) · sunnysavita Classes 1–16 | `01-foundations-agents` |
| **2. LangGraph Core** | 2–3 weeks | StateGraph, conditional edges, parallel + reducers, tools, memory, HITL, subgraphs | [sourangshupal 01–06](https://github.com/sourangshupal/langraph-tutorials) · [Telusko Getting Started with LangGraph](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Getting%20Started%20with%20LangGraph%2017-10-2026) + Types of Graphs | `02` + `03` + `05` |
| **3. Agentic RAG** | 1–2 weeks | Corrective/Adaptive loops, hybrid + rerank, evaluation | [Telusko RAG Fundamentals](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/RAG%20Fundamentals%20and%20Production%20Techniques%2027-09-2026) · [Complete RAG](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Building%20a%20Complete%20RAG%20Application%2004-10-2026) · [Secure Enterprise RAG](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Secure%20Enterprise%20RAG%20Assistant%2010-10-2026) · Ultimate RAG Bootcamp | `04-agentic-rag` |
| **4. Advanced Control + MCP** | 1–2 weeks | Command, Send, dynamic nodes, MCP servers/clients/adapters | [Telusko Advance LangGraph](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Advance%20LangGraph%2014-11-2026) · [sourangshupal 08](https://github.com/sourangshupal/langraph-tutorials/blob/main/08_command_functional_api_longterm_memory.ipynb) · [MCP Part-2/3/4](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/MCP%20(Part%20-%202)%2013-09-2026) · MCP path | `06` + `07-mcp-integration` |
| **5. Multi-Agent + Production** | 1–2 weeks | Orchestrator-worker, guardrails, observability, streaming, durable checkpoints | [sourangshupal 07](https://github.com/sourangshupal/langraph-tutorials/blob/main/07_production_patterns_advanced_features.ipynb) · [09](https://github.com/sourangshupal/langraph-tutorials/blob/main/09_multi_agent_systems.ipynb) · [10](https://github.com/sourangshupal/langraph-tutorials/blob/main/10_testing_observability_platform.ipynb) · sunnysavita Classes 49–59 | `06` + `08-projects-and-interview` |

---

## 🏆 Must-Do Projects (Cross-Repo Priority)

These give the highest interview and production ROI. Complete them in roughly this order. Full details live in [`08-projects-and-interview/MUST-DO-PROJECTS.md`](../08-projects-and-interview/MUST-DO-PROJECTS.md).

| # | Project | Skills | Direct Links to Start |
|---|---------|--------|-----------------------|
| 1 | Simple StateGraph with conditional edge | Core LangGraph | [sourangshupal 01](https://github.com/sourangshupal/langraph-tutorials/blob/main/01_introduction_to_langgraph.ipynb) · [02](https://github.com/sourangshupal/langraph-tutorials/blob/main/02_conditional_routing.ipynb) · [Telusko Getting Started with LangGraph](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Getting%20Started%20with%20LangGraph%2017-10-2026) |
| 2 | Parallel + Reducer graph | Fan-out / merge | [Telusko Advance reducers (11–15)](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Advance%20LangGraph%2014-11-2026) · [sourangshupal 06](https://github.com/sourangshupal/langraph-tutorials/blob/main/06_parallel_execution_subgraphs.ipynb) |
| 3 | ReAct multi-tool agent | Tool calling + routing | [Telusko LangChain Tools and Agents](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/LangChain%20Tools%20and%20Agents%2030-08-2026) · [Tool Calling Part-2](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Tool%20Calling%20(Part-2)%20-%2005-09-2026) · [sourangshupal 03](https://github.com/sourangshupal/langraph-tutorials/blob/main/03_tool_integration_openai.ipynb) |
| 4 | Agentic/Corrective RAG loop | Self-correcting retrieval | [Telusko RAG Fundamentals](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/RAG%20Fundamentals%20and%20Production%20Techniques%2027-09-2026) · [Complete RAG](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Building%20a%20Complete%20RAG%20Application%2004-10-2026) · [RAG Evaluation](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/RAG%20Evaluation%20and%20Production%20Techniques%2003-10-2026) · Stage 04 |
| 5 | HITL approval agent (durable) | Interrupts + SqliteSaver | [Telusko Types of Graphs Part-2](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Types%20of%20Graphs%20(Part%20-%202)%2031-10-2026) · [Part-3](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Types%20of%20Graphs%20(Part%20-%203)%2001-11-2026) · [Part-4](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Types%20of%20Graphs%20(Part%20-%204)%2007-11-2026) · [sourangshupal 05](https://github.com/sourangshupal/langraph-tutorials/blob/main/05_human_in_the_loop_streaming.ipynb) |
| 6 | Subgraph workflow | Composition | [Telusko Advance subgraphs](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Advance%20LangGraph%2014-11-2026) · [sourangshupal 06](https://github.com/sourangshupal/langraph-tutorials/blob/main/06_parallel_execution_subgraphs.ipynb) · [app/06_subgraphs.py](https://github.com/sourangshupal/langraph-tutorials/blob/main/app/06_subgraphs.py) |
| 7 | MCP-powered agent | Standardized tools | [Telusko MCP Part-2](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/MCP%20(Part%20-%202)%2013-09-2026) · [Part-3](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/MCP%20(Part%20-3)%2019-09-2026) · [Part-4](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/MCP%20(Part%20-%204)%2020-09-2026) · [Support App with MCP](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Building%20a%20Support%20App%20with%20MCP%2011-10-2026) · [mcp-learning-path](https://github.com/yash9614/mcp-learning-path) |
| 8 | Multi-agent research/support system | Orchestration | [sourangshupal 09](https://github.com/sourangshupal/langraph-tutorials/blob/main/09_multi_agent_systems.ipynb) · [app/07_multiagent.py](https://github.com/sourangshupal/langraph-tutorials/blob/main/app/07_multiagent.py) · [07](https://github.com/sourangshupal/langraph-tutorials/blob/main/07_production_patterns_advanced_features.ipynb) |
| 9 | Production RAG with eval + hybrid | Real retrieval quality | [Telusko Secure Enterprise RAG](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Secure%20Enterprise%20RAG%20Assistant%2010-10-2026) · [Complete RAG](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Building%20a%20Complete%20RAG%20Application%2004-10-2026) · [RAG Evaluation](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/RAG%20Evaluation%20and%20Production%20Techniques%2003-10-2026) |
| 10 | Full support app (MCP + HITL + memory) | End-to-end | [Telusko Building a Support App with MCP](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/Building%20a%20Support%20App%20with%20MCP%2011-10-2026) · Advance HITL + memory programs |

---

## 🔑 Concept Cheat Sheet

| Term | One-Liner | Jump To |
|------|-----------|---------|
| **State** | Shared TypedDict / Pydantic model that flows through nodes | [sourangshupal 01](https://github.com/sourangshupal/langraph-tutorials/blob/main/01_introduction_to_langgraph.ipynb) |
| **Reducer** | Merges parallel writes to the same field (`Annotated[list, operator.add]`) | Telusko Advance 11–15 |
| **Command** | `Command(update=..., goto=..., resume=...)` — explicit control + interrupt resume | [sourangshupal 08](https://github.com/sourangshupal/langraph-tutorials/blob/main/08_command_functional_api_longterm_memory.ipynb) · [app/05_send_command.py](https://github.com/sourangshupal/langraph-tutorials/blob/main/app/05_send_command.py) |
| **Send** | Dynamic fan-out (map-reduce style) | Telusko Advance 38+ · [app/01_send_basic.py](https://github.com/sourangshupal/langraph-tutorials/blob/main/app/01_send_basic.py) |
| **Checkpointer** | Persists state for memory + HITL (`InMemorySaver`, `SqliteSaver`) | [sourangshupal 04](https://github.com/sourangshupal/langraph-tutorials/blob/main/04_state_persistence_and_memory.ipynb) |
| **HITL** | Interrupt → human input → resume (can be in nodes or tools) | [sourangshupal 05](https://github.com/sourangshupal/langraph-tutorials/blob/main/05_human_in_the_loop_streaming.ipynb) |
| **Agentic RAG** | Agent decides whether/how to retrieve, can rewrite & retry | Telusko RAG modules |
| **CRAG / Self-RAG** | Grade retrieval and correct, or model decides whether to retrieve | Stage 04 + Ultimate RAG |
| **MCP** | Standard protocol for exposing tools as servers (stdio / SSE / Streamable HTTP) | [Telusko MCP](https://github.com/telusko-aliens/agentic-ai-engineering-with-python/tree/main/MCP%20(Part%20-%202)%2013-09-2026) · [mcp-learning-path](https://github.com/yash9614/mcp-learning-path) |
| **Subgraph** | Graph used as a node or invoked inside another graph (state mapping matters) | [sourangshupal 06](https://github.com/sourangshupal/langraph-tutorials/blob/main/06_parallel_execution_subgraphs.ipynb) · Telusko Advance |

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
- [sourangshupal full series](https://github.com/sourangshupal/langraph-tutorials)
- [Telusko full course repo](https://github.com/telusko-aliens/agentic-ai-engineering-with-python)

---

**Last updated:** 21 November 2026  
**Purpose:** Cross-repo compass for this learning path. Keep it updated when new high-signal resources appear.

Happy building agents! 🤖
