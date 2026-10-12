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
| This repo | Agentic systems, LangGraph, agents, HITL, workflows | You are here |

**Recommended order:** GenAI foundations → RAG depth → Agentic systems (this repo) → MCP integration.

---

## Learning Path Overview

| Stage | Folder | Focus | Priority |
|-------|--------|-------|----------|
| 1 | `01-foundations-agents` | Agents vs Agentic AI, core concepts | High |
| 2 | `02-langgraph-basics` | State graphs, nodes, edges, simple graphs | High |
| 3 | `03-react-and-tool-calling` | ReAct agents, multi-tool chatbots | Critical |
| 4 | `04-agentic-rag` | Corrective, Adaptive, Agentic RAG loops | Critical |
| 5 | `05-human-in-the-loop` | HITL patterns, interrupts, approvals | High |
| 6 | `06-workflows-and-routing` | Workflows, routers, multi-step systems | High |
| 7 | `07-mcp-integration` | LangGraph + MCP, tool servers | High |
| 8 | `08-projects-and-interview` | Must-do projects + interview Q bank | Critical |

Work the folders in order. Each has a detailed README with concepts, what to study, interview questions, and links back to source notebooks.

---

## Must-Do Projects (Priority Order)

These give the highest ROI for interviews and real systems. Complete them.

1. **Simple LangGraph State Graph** — Understand nodes, edges, state.
2. **ReAct Tool-Calling Agent** — Wikipedia / Arxiv / search tools with conditional routing.
3. **Agentic / Corrective RAG Loop** — Grade documents, rewrite query, retrieve again.
4. **Human-in-the-Loop Approval Agent** — Interrupt for sensitive actions.
5. **Multi-Tool Chatbot with Routing** — Route between vector store, web search, SQL.
6. **MCP-Enabled Agent** — Expose tools via MCP and call them from LangGraph.
7. **End-to-End Workflow** (optional) — News agent, blog generator, or multi-agent research.

Details and source file pointers are in `08-projects-and-interview/MUST-DO-PROJECTS.md`.

---

## Key Concepts You Must Master

- Agent vs Agentic AI
- ReAct (Reason + Act) pattern
- LangGraph StateGraph, nodes, edges, conditional edges
- Tool calling / function calling
- State management (TypedDict, dataclass, Pydantic)
- Agentic RAG loops (grade → rewrite → retrieve)
- Human-in-the-loop (interrupts, checkpoints)
- Routing and multi-agent patterns
- Memory and persistence
- MCP (Model Context Protocol) as tool interface

---

## Setup

```bash
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
pip install langchain langgraph langchain-community langchain-openai
# Add more as needed per notebook
```

Use `.env` for API keys. Never hardcode them.

---

## How to Use This Repo

1. Read each module README carefully (concepts + interview questions).
2. Open the linked notebooks from the original dump and run them.
3. Complete the Must-Do Projects.
4. Practice the interview questions out loud.
5. Cross-reference the RAG and GenAI repos for deeper foundations.

Start with `01-foundations-agents/README.md`.

Happy building agents!
