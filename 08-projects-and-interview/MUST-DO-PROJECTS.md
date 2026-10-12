# Must-Do Projects

Complete these in order. They map directly to common interview expectations.

## 1. Simple State Graph
**Goal:** Master LangGraph fundamentals.  
**Source:** `1-simplegraph.ipynb`  
**Deliverable:** A working graph with at least one conditional edge.

## 2. ReAct Tool-Calling Agent
**Goal:** Production-style agent with tools.  
**Source:** `7-ReActAgents.ipynb` + multi-tool chatbot notebooks  
**Deliverable:** Agent that uses 2+ tools and stops correctly.

## 3. Agentic / Corrective RAG
**Goal:** Retrieval that can self-correct.  
**Source:** `1-AgenticRAG.ipynb`, `2-CorrectiveRAG.ipynb`, `4-AdaptiveRAG.ipynb`  
**Deliverable:** Grade → rewrite → re-retrieve loop.

## 4. Human-in-the-Loop Agent
**Goal:** Safe agents.  
**Source:** `1-Humanintheloop.ipynb`  
**Deliverable:** Approval gate on a sensitive action.

## 5. Routing Agent / Multi-Source
**Goal:** Intelligent tool/source selection.  
**Deliverable:** Router between vector DB and web search.

## 6. MCP-Powered Agent
**Goal:** Modern tool architecture.  
**Sources:** `mcplanggraph` folder + [MCP_PROJECTS_oo3](https://github.com/yash9614/MCP_PROJECTS_oo3)  
**Deliverable:** LangGraph agent calling tools via MCP.

## 7. Capstone (Optional but Impressive)
Pick one:
- AI News Agent (`ainewsagentic`)
- Blog Generation pipeline
- Multi-agent research system

---

**Interview tip:** Be ready to explain the design decisions, failure modes, and how you would productionize each project (observability, evaluation, cost control, guardrails).
