# 04 — Agentic RAG

## Core Concepts

Naive RAG = retrieve once → generate.

**Agentic RAG** adds decision loops:
- Grade retrieved documents (are they relevant?)
- Rewrite the query if not
- Retrieve again
- Optionally fall back to web search
- Self-reflect on the answer

Common variants: Corrective RAG (CRAG), Adaptive RAG, Self-RAG.

## Production Retrieval Inside Agentic Loops

The loop is only as good as the retrieval underneath it. Combine with:

- Hybrid search (dense + BM25) + Reciprocal Rank Fusion
- Cross-encoder reranking
- Metadata filters
- Query transformation (rewrite, step-back, multi-query, decomposition)
- Parent-child / contextual chunking
- Citations in the final answer
- Evaluation: Hit@K + RAGAS (Faithfulness, Answer Relevancy, Context Precision/Recall, Answer Correctness)

**Production guide:** [PRODUCTION-RAG-GUIDE.md](https://github.com/yash9614/generative-ai-learning-path/blob/main/03-RAG-Systems/PRODUCTION-RAG-GUIDE.md)

**Handbook extract:** [reference/PYTHON-FOR-GENAI-CONCEPTS.md](../reference/PYTHON-FOR-GENAI-CONCEPTS.md) (hybrid RRF, parent-child chunking, GraphRAG, RAGAS)

## External Resources

- RAGAS: [divesh-sse/RAGAS](https://github.com/divesh-sse/RAGAS)
- Query transformations: [d-hackmt/query-transformations](https://github.com/d-hackmt/query-transformations)
- Production toolkit: [laxmimerit/RAGWire](https://github.com/laxmimerit/RAGWire)
- Local agentic RAG: [laxmimerit/Agentic-RAG-with-LangGraph-and-Ollama](https://github.com/laxmimerit/Agentic-RAG-with-LangGraph-and-Ollama)
- CRAG / Self-RAG: [entbappy/Complete-Agentic-AI-Course](https://github.com/entbappy/Complete-Agentic-AI-Course)
- Advanced RAG: [sunnysavita10/Generative-AI-Indepth-Basic-to-Advance](https://github.com/sunnysavita10/Generative-AI-Indepth-Basic-to-Advance)

See also `reference/EXTERNAL-RAG-RESOURCES.md` and `reference/EXTERNAL-SCANNED-RESOURCES.md`.

## Course Mapping (Telusko)

- `Embeddings and Vector Stores 26-09-2026`
- `RAG Fundamentals and Production Techniques 27-09-2026`
- `RAG Evaluation and Production Techniques 03-10-2026`
- `Building a Complete RAG Application 04-10-2026`
- `Secure Enterprise RAG Assistant 10-10-2026`

## Key Notebooks

- `1-AgenticRAG.ipynb`
- `2-CorrectiveRAG.ipynb`
- `4-AdaptiveRAG.ipynb`

**Cross-link:** [Ultimate-RAG-Bootcamp](https://github.com/yash9614/Ultimate-RAG-Bootcamp-LangChain-LangGraph-LangSmith)

## Interview Questions

1. What is Agentic RAG and why is it better than naive RAG?
2. Explain the Corrective RAG flow.
3. How do you grade documents for relevance?
4. When would you rewrite a query vs fall back to web search?
5. How do you prevent infinite retrieval loops?
6. Name at least three RAGAS metrics and what they measure.
7. How does hybrid search + reranking improve the documents you grade?
8. Why are stable chunk IDs and metadata important in production?
9. Name three query transformation techniques and when to use each.
10. What is parent-child chunking and when does it help?

## Must-Do

Implement a grade → rewrite → retrieve loop. Compare to simple RAG.  
Upgrade with hybrid search + cross-encoder reranking and measure with a small evaluation set. Optionally add multi-query or step-back.
