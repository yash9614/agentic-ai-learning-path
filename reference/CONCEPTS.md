# Concept Glossary — Agentic AI

| Term | Meaning |
|------|---------|
| **Agent** | LLM + tools + decision loop (brain + hands) |
| **ReAct** | Reason → Act → Observe loop |
| **LangGraph** | Explicit state graph (nodes, edges, conditional routing, checkpointers) |
| **State** | Shared data structure nodes read/write |
| **Node** | Function that returns a partial state update |
| **Conditional Edge** | Router that decides next node |
| **Checkpointer** | Persists state for memory and HITL |
| **CrewAI** | Role-based multi-agent (Agent + Task + Crew + Process) |
| **Deep Agents** | Opinionated harness (planning, filesystem, subagents) on LangChain + LangGraph |
| **Agentic RAG** | Agent controls retrieval (decide, decompose, re-retrieve) |
| **CRAG** | Grades retrieval and corrects (rewrite / web search) |
| **Self-RAG** | Model decides whether to retrieve and critiques its own answer |
| **MCP** | Standard protocol for tool servers |
| **HITL** | Human-in-the-loop via interrupts |
| **Harness** | Guardrails, step limits, validation, observability around the model |

## Stack Layers

- LangGraph = runtime
- LangChain = framework
- Deep Agents = harness
- CrewAI = role-based team abstraction

Deeper notes: [makan_m/learning-concepts](https://github.com/yash9614/makan_m/tree/main/learning-concepts) (modules 10–20)
