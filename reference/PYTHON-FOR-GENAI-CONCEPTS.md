# Python for Gen AI — Clean Concept Extract

Source: *Python for Gen AI* (500-page handbook). Extracted for technical understanding only. No culinary analogies.

## Curriculum Overview (24 Chapters)

| Part | Chapters | Core Topics |
|------|----------|-------------|
| I–II Core | 1–9 | Python fundamentals, AsyncIO, NumPy, Pandas, BPE/tokenizers, embeddings, vector DBs (Chroma/FAISS, HNSW, hybrid RRF) |
| III LLMs | 10–13 | Frontier SDKs (OpenAI/Gemini), sampling, advanced prompting, structured outputs (Pydantic), tool calling |
| IV RAG & Agents | 14–17 | Production RAG & chunking, hybrid search + reranking, LangGraph + MCP agents, multi-agent systems |
| V MLOps | 18–20 | PyTorch + LoRA/QLoRA, RAGAS evaluation + guardrails, FastAPI + SSE + semantic cache |
| VI Frontier | 21–24 | Reasoning models (o3/R1), realtime voice/WebSockets, GraphRAG, vLLM/quantization/FinOps |

## Key Technical Concepts to Internalize

### Python & Systems
- Type hints, dataclasses, generators (`yield`), decorators, closures, LRU cache
- AsyncIO: `TaskGroup`, semaphores, non-blocking concurrent LLM calls
- Pydantic v2: schema validation, constrained decoding, validators for LLM outputs

### Vectors & Retrieval
- Embeddings, BPE (tiktoken), Matryoshka embeddings
- Vector DBs: HNSW indexing, pre-filtering, hybrid search (BM25 + dense) + Reciprocal Rank Fusion (RRF)
- Cross-encoder reranking, MMR
- Production chunking: contextual headers, parent-child RAG

### LLMs & Prompting
- Sampling: temperature, top_p, SSE streaming, KV prefix caching
- Advanced prompting: structured XML, k-NN few-shot, Chain-of-Thought
- Structured outputs and tool calling (parallel tools, HITL gates)

### Agents
- LangGraph: cyclic StateGraph, checkpoints, MCP tool integration
- Multi-agent: supervisor, map-reduce, handoffs
- Memory: short-term (checkpointer) vs long-term (store)

### Production & Evaluation
- LoRA / QLoRA, PEFT, DPO
- RAGAS: Faithfulness, Answer Relevancy, Context Precision/Recall, Answer Correctness
- Guardrails: input validation, PII filtering, de-biased judges
- FastAPI: lifespan pools, semantic cache, SSE streaming
- Reasoning models: test-time compute, process reward models
- GraphRAG: triples, multi-hop walks, communities
- Serving: vLLM, PagedAttention, AWQ quantization, FinOps

## Suggested Reading Tracks

1. **Full path:** Chapters 1–24 sequentially.
2. **Backend engineer entering GenAI:** Skim 1–4, start deep at Chapter 5 (AsyncIO + Pydantic), continue through 24.
3. **Staff / Principal interview prep:** Sections on system design and interview grills in each chapter + Part VI (21–24).

## High-Priority Interview Topics from the Book

- Hybrid search (BM25 + dense + RRF) vs pure vector search
- Parent-child / contextual chunking strategies
- LangGraph cyclic graphs, checkpoints, and MCP integration
- Multi-agent supervisor vs map-reduce patterns
- RAGAS metrics and how to prevent judge bias
- LoRA/QLoRA vs full fine-tuning trade-offs
- Semantic caching in FastAPI + SSE streaming
- GraphRAG multi-hop reasoning
- vLLM / PagedAttention for high-throughput serving
- Test-time compute in reasoning models (o3 / R1)

## How to Use with the Learning Paths

- Foundations & vectors → generative path `01-Foundations` and `03-RAG-Systems`
- Agents & LangGraph → agentic path `02`–`06` and generative `04-Agents-and-LangGraph`
- Evaluation & production → agentic `04` (RAGAS) and generative production guide
- Frontier topics (GraphRAG, reasoning, voice, vLLM) → optional advanced reading after core stages

Cross-reference existing files: `EXTERNAL-RAG-RESOURCES.md`, `TELUSKO-SESSION-MAP.md`, `SUNNYSAVITA-FULLSTACK-GENAI-BOOTCAMP.md`.
