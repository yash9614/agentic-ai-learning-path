# Python for Gen AI — Clean Concept Extract

Source: *Python for Gen AI* (500-page handbook). Technical concepts and interview framing only. No analogies.

## Curriculum Map (24 Chapters)

| Part | Chapters | Focus |
|------|----------|-------|
| I–II Core | 1–9 | Python, AsyncIO, NumPy/Pandas, tokenizers (BPE), embeddings, vector DBs (HNSW, hybrid RRF) |
| III LLMs | 10–13 | SDKs, sampling, prompting, structured outputs (Pydantic), tool calling |
| IV RAG & Agents | 14–17 | Production RAG & chunking, hybrid + rerank, LangGraph + MCP, multi-agent |
| V MLOps | 18–20 | LoRA/QLoRA, RAGAS + guardrails, FastAPI + SSE + semantic cache |
| VI Frontier | 21–24 | Reasoning models, voice/WebSockets, GraphRAG, vLLM / quantization / FinOps |

## Core Patterns (Prioritized)

### Retrieval
- Hybrid search: dense + BM25 + Reciprocal Rank Fusion (RRF)
- Cross-encoder reranking, MMR
- Production chunking: contextual headers, parent-child RAG
- Pre-filtering + HNSW in Chroma/FAISS

### Agents
- Cyclic LangGraph StateGraph with checkpoints
- MCP tool integration
- Multi-agent: supervisor, map-reduce, handoffs
- Short-term memory (checkpointer + thread_id) vs long-term (store + user_id)

### Production & Evaluation
- RAGAS: Faithfulness, Answer Relevancy, Context Precision/Recall, Answer Correctness
- Guardrails: input validation, PII filtering, de-biased judges
- LoRA / QLoRA vs full fine-tuning
- FastAPI lifespan pools + semantic cache + SSE
- GraphRAG: triples, multi-hop walks, community detection
- Serving: vLLM, PagedAttention, AWQ
- Reasoning models: test-time compute, process reward models

### Systems Foundations
- AsyncIO (`TaskGroup`, semaphores) for concurrent LLM calls
- Pydantic v2 for structured outputs and validation
- Generators, decorators, type hints

## Reading Tracks

| Track | Approach |
|-------|----------|
| Full | Chapters 1–24 in order |
| Backend → GenAI | Skim 1–4; start deep at Chapter 5 (AsyncIO + Pydantic); continue through 24 |
| Staff / Principal | System-design and interview sections of each chapter + Part VI (21–24) |

## Mapping to Learning Paths

| Handbook Topics | Agentic Path | Generative Path |
|-----------------|--------------|-----------------|
| Vectors, hybrid RRF, chunking | `04-agentic-rag` | `03-RAG-Systems` + PRODUCTION-RAG-GUIDE |
| LangGraph, MCP, multi-agent | `02`, `03`, `06`, `07` | `04-Agents-and-LangGraph` |
| RAGAS, guardrails | `04`, `08` | `03-RAG-Systems` |
| Fine-tuning (LoRA) | Optional | `06-Fine-tuning-HuggingFace` |
| Frontier (GraphRAG, reasoning, vLLM) | Optional advanced | Optional advanced |

## Related Files in This Repo

- [EXTERNAL-RAG-RESOURCES.md](EXTERNAL-RAG-RESOURCES.md)
- [TELUSKO-SESSION-MAP.md](TELUSKO-SESSION-MAP.md)
- [SUNNYSAVITA-FULLSTACK-GENAI-BOOTCAMP.md](SUNNYSAVITA-FULLSTACK-GENAI-BOOTCAMP.md)
- [ENTBAPPY-RESOURCES.md](ENTBAPPY-RESOURCES.md)
- Interview bank: `08-projects-and-interview/INTERVIEW-QUESTIONS.md`

## High-Priority Interview Topics

1. Hybrid search (BM25 + dense + RRF) vs pure vector
2. Parent-child / contextual chunking
3. Cyclic LangGraph + checkpoints + MCP
4. Supervisor vs map-reduce multi-agent
5. RAGAS metrics and judge bias
6. LoRA/QLoRA vs full fine-tuning
7. Semantic caching with FastAPI + SSE
8. GraphRAG multi-hop vs standard vector RAG
9. vLLM / PagedAttention
10. Test-time compute in reasoning models

Use this file as a concept index. Dive into the linked stage READMEs and external repos for implementation detail.
