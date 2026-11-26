# entbappy Resources — Multi-Agent & Agentic RAG

High-value projects from [entbappy](https://github.com/entbappy). Use alongside Telusko Final Project and the existing external references.

## Top Projects

| Repo | Stars | Key patterns |
|------|-------|--------------|
| [Complete-Agentic-AI-Course](https://github.com/entbappy/Complete-Agentic-AI-Course) | 279 | Advanced RAG, CRAG, Self-RAG, LangGraph, multi-agent research, interview prep PDFs |
| [Multi-Agent-System-using-LangGraph-MCP-Supervisor-Guardrails-HITL](https://github.com/entbappy/Multi-Agent-System-using-LangGraph-MCP-Supervisor-Guardrails-HITL) | 42 | Supervisor + MCP tools + input guardrails + HITL approval + FastAPI |
| [Enterprise-IT-Support-Agentic-RAG-Copilot](https://github.com/entbappy/Enterprise-IT-Support-Agentic-RAG-Copilot) | 33 | Private KB (Pinecone) → grade evidence → fallback to web search → rewrite + retry, decision logging |
| [Enterprise-HR-Policy-Employee-Support-Agentic-RAG-Copilot](https://github.com/entbappy/Enterprise-HR-Policy-Employee-Support-Agentic-RAG-Copilot) | 15 | Similar agentic RAG pattern for HR policy |
| [TripMate-AI-A-Multi-Agent-Travel-Planner-with-LangGraph](https://github.com/entbappy/TripMate-AI-A-Multi-Agent-Travel-Planner-with-LangGraph) | 29 | Multi-agent travel planner |
| [LangChain-Multi-Agent-Research-System](https://github.com/entbappy/LangChain-Multi-Agent-Research-System) | 8 | Multi-agent research |

## Interview-relevant patterns

- **Supervisor + specialists** with MCP tools and HITL approval gates.
- **Input guardrails** before the graph runs.
- **Agentic RAG with fallback**: grade private evidence → if weak, web search → grade again → rewrite query and retry (with limits).
- **Decision logging** for auditability (SQLite).
- **Agent isolation**: specialists only see the request and their own tools.

## How to use

- After Telusko Final Project → study the Multi-Agent-System-using-LangGraph-MCP-Supervisor-Guardrails-HITL for guardrails + HITL on top of supervisor + MCP.
- For enterprise RAG → run or read the IT Support copilot (private KB + web fallback + grading).
- Interview prep PDFs are in Complete-Agentic-AI-Course/Agentic AI Interview Preparation.
