# External LangGraph Tutorials — Essential Patterns

Two high-quality complementary series. Use them alongside the Telusko course.

## 1. sourangshupal/langraph-tutorials
**10 progressive notebooks (LangGraph ~1.1.9)**

| # | Notebook theme | What to extract |
|---|----------------|-----------------|
| 01 | Introduction | Basic StateGraph, nodes, edges |
| 02 | Conditional routing | tools_condition style routing |
| 03 | Tool integration (OpenAI) | bind_tools + ToolNode |
| 04 | State persistence & memory | Checkpointers, thread_id |
| 05 | HITL + streaming | interrupt + stream modes |
| 06 | Parallel execution & subgraphs | Fan-out, subgraph as node |
| 07 | Production patterns | Error handling, limits, observability hooks |
| 08 | Command / functional API / long-term memory | Command(update/goto), long-term store |
| 09 | Multi-agent systems | Supervisor / peer patterns |
| 10 | Testing & observability | LangSmith, unit testing graphs |

**Projects mentioned:** customer support bot with memory, research assistant with HITL, multi-agent research system, enterprise support system.

## 2. d-hackmt/langgraph-life
**Hands-on notebooks + 22 diagrams + interactive deck**

| Folder | Focus |
|--------|-------|
| 01-langgraph-basics | StateGraph, nodes, edges, conditional, reducers, first chatbot |
| 02-langgraph-components | Streaming, state schemas, tools, ReAct, memory |
| 03-debugging | langgraph.json, langgraph dev, Studio |
| 04-workflows | Prompt chaining, parallelization, routing, orchestrator-worker, evaluator-optimizer |
| 05-human-in-the-loop | Breakpoints, interrupt(), Command(resume) |
| 06-rag | Agentic, Corrective, Adaptive RAG |
| 07-multimodal | Page-image RAG with Gemini embeddings |
| 08-end to end | Full applications |
| 09-mcp | MCP integration |

**Special:** Interactive deck at d-hackmt.github.io/langgraph-life (laser pointer, code panels, quizzes). Diagrams at the top of every notebook.

## How to use with this learning path

- **02-langgraph-basics** → notebooks 01–04 + d-hackmt 01–02
- **03-react-and-tool-calling** → notebook 03 + d-hackmt 02
- **05-human-in-the-loop** → notebook 05 + d-hackmt 05
- **06-workflows-and-routing** → notebook 06/09 + d-hackmt 04
- **04-agentic-rag** → d-hackmt 06
- **07-mcp-integration** → d-hackmt 09

Clone both repos locally and run the notebooks after the corresponding Telusko session.
