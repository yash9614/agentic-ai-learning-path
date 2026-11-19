# 04 — Agentic RAG

## Core Concepts

Naive RAG = retrieve once → generate.  

**Agentic RAG** adds decision loops:

- Grade retrieved documents (are they relevant?)
- Rewrite the query if not
- Retrieve again
- Possibly use web search as fallback
- Self-reflect on the answer

Variants you will see:
- Corrective RAG (CRAG)
- Adaptive RAG
- Self-reflective RAG

## Course Mapping (Telusko)

Production RAG progression lives in these folders:
- `Embeddings and Vector Stores 26-09-2026`
- `RAG Fundamentals and Production Techniques 27-09-2026`
- `RAG Evaluation and Production Techniques 03-10-2026`
- `Building a Complete RAG Application 04-10-2026`
- `Secure Enterprise RAG Assistant 10-10-2026`

These cover hybrid search, metadata filters, reranking, corrective/adaptive patterns, citation, and evaluation.

## Key Notebooks

- `1-AgenticRAG.ipynb`
- `2-CorrectiveRAG.ipynb`
- `4-AdaptiveRAG.ipynb`
- PDFs: `35-39-RAGS.pdf`, `37.1-Corrective+RAGs.pdf`

**Cross-link:** Deep RAG foundations are in [Ultimate-RAG-Bootcamp](https://github.com/yash9614/Ultimate-RAG-Bootcamp-LangChain-LangGraph-LangSmith) (especially modules 06 and 07).

## Interview Questions

1. What is Agentic RAG and why is it better than naive RAG?
2. Explain the Corrective RAG flow.
3. How do you grade documents for relevance?
4. When would you rewrite a query vs fall back to web search?
5. How do you prevent infinite retrieval loops?
6. What evaluation metrics matter for an agentic RAG system?

## Must-Do

Implement a grade → rewrite → retrieve loop. Compare answer quality to simple RAG. Optionally add hybrid search or reranking from the production RAG folders.
