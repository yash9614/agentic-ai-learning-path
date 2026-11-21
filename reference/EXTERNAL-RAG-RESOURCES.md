# External RAG Resources — Essential Patterns

Complementary repos for production RAG and evaluation. Use with the Telusko RAG sessions and Ultimate-RAG-Bootcamp.

## 1. divesh-sse/RAGAS
**Practical RAGAS evaluation**

- Learning notebook (`evals.ipynb`) that isolates each metric with hand-crafted failure modes.
- Six metrics:
  - Faithfulness (grounded in context)
  - Answer Relevancy
  - Context Precision (ranking)
  - Context Recall
  - Answer Correctness
  - Tool Correctness (Jaccard, no LLM judge)
- Two-phase pipeline: run RAG on goldens → score with RAGAS (with rate-limit handling and checkpointing).
- Streamlit app for end-to-end demo (Gemini embeddings + Groq LLM).
- Files: `goldens.json`, `EVALS.md`, diagrams.

**Use for:** Stage 04 (Agentic RAG) evaluation section.

## 2. d-hackmt/query-transformations
**Query transformation techniques (pre-retrieval)**

Notebook + docs covering:
- Query rewriting
- Step-back prompting
- Sub-query decomposition
- Multi-query generation + Reciprocal Rank Fusion
- Query routing
- Query compression
- Contextual query enhancement
- Query translation to filters
- Agentic RAG (LangGraph) that chooses the transformation

**Use for:** Improving retrieval before the agentic grade/rewrite loop.

## 3. laxmimerit repos (selected)

| Repo | Focus | Key takeaways |
|------|-------|---------------|
| **RAGWire** | Production RAG toolkit | PDF/DOCX/XLSX → Qdrant, LLM metadata extraction, hybrid search, SHA256 dedup (file + chunk), metadata filters, CLI |
| **Agentic-RAG-with-LangGraph-and-Ollama** | Full local stack | LangGraph + Ollama (privacy), ReAct, short/long-term memory, interrupts, reflection agent, MySQL agent, MCP |
| **Langchain-v1-Agents** | Local agents | ReAct, agentic RAG with grading/rewriting, multi-agent (supervisor + specialists + rerank), short/long-term memory, HITL middleware |
| **Langchain-10-Days-Bootcamp** | Beginner | Free APIs, RAG over 10-K filings with citations |

**Use for:** Production patterns, local/private models, and concrete agentic RAG implementations.

## How to use with this path

- After Telusko RAG folders → run query-transformations notebook, then RAGAS eval notebook.
- For local/private work → follow laxmimerit Agentic-RAG-with-LangGraph-and-Ollama or Langchain-v1-Agents.
- For production ingestion → study RAGWire’s hybrid + metadata + dedup approach.
