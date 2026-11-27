# RAGAS Evaluation Metrics

RAGAS (Retrieval-Augmented Generation Assessment) scores a RAG pipeline by separating **retrieval quality** from **generation quality**. Most metrics use an LLM judge; some also use embeddings. Scores are typically 0–1 (higher is better).

Official docs: https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/

## Core Metrics

| Metric | What it measures | Needs reference? | Stage |
|--------|------------------|------------------|-------|
| **Faithfulness** | Fraction of claims in the answer that are supported by the retrieved context | No | Generation (hallucination) |
| **Response Relevancy** (Answer Relevancy) | How well the answer addresses the original question | No | Generation |
| **Context Precision** | Whether relevant chunks are ranked near the top | Optional (reference or response) | Retrieval (ranking) |
| **Context Recall** | Fraction of claims in the reference answer that appear in the retrieved context | Yes | Retrieval (coverage) |
| **Answer Correctness** | Factual overlap (F1) + semantic similarity vs ground truth | Yes | End-to-end |

## How Key Metrics Are Calculated

### Faithfulness
1. Extract atomic claims from the generated answer.
2. For each claim, ask an LLM judge whether it can be inferred from the retrieved context.
3. Score = (supported claims) / (total claims).

Example: 1 of 2 claims supported → 0.5.

### Response Relevancy
1. From the answer, generate several questions the answer would address (default ~3).
2. Embed those questions and the original question.
3. Score = average cosine similarity between generated questions and the original question.

### Context Precision
For each retrieved chunk, an LLM judges whether it is useful for the question. The score is a rank-weighted average of precision at each relevant rank (relevant chunks higher in the list contribute more).

### Context Recall
1. Extract claims from the reference (ground-truth) answer.
2. Check how many of those claims can be attributed to the retrieved context.
3. Score = (reference claims found in context) / (total reference claims).

### Answer Correctness
Weighted combination of:
- **Factual Correctness** (F1 over TP/FP/FN facts vs ground truth):
  \[
  F1 = \frac{|TP|}{|TP| + 0.5 \times (|FP| + |FN|)}
  \]
- **Semantic Similarity** (embedding similarity to ground truth).

Weights are configurable.

## Diagnostic Guide

| Low score | Likely problem | Typical fix |
|-----------|----------------|-------------|
| Context Precision | Irrelevant chunks ranked high | Reranker, better embeddings, metadata filters |
| Context Recall | Missing relevant chunks | Larger top-k, better chunking, query rewrite |
| Faithfulness | Hallucination beyond context | Stronger grounding prompt, better model |
| Response Relevancy | Off-topic or incomplete answer | Prompt constraints, temperature |
| Answer Correctness | Wrong or incomplete vs ground truth | Both retrieval and generation issues |

## Other Metrics

- Context Entities Recall, Noise Sensitivity
- Multimodal Faithfulness / Relevance
- Factual Correctness, Semantic Similarity (standalone)
- Non-LLM: BLEU, ROUGE, exact match, string similarity
- NVIDIA-contributed: Answer Accuracy, Context Relevance, Response Groundedness

## Practical Notes

- Faithfulness and Response Relevancy can run on live traffic (no golden set required).
- Context Recall and Answer Correctness need reference answers.
- LLM judges introduce variance and cost; use consistent judge models and consider de-biasing techniques.
- Pair with retrieval metrics (Hit@K, MRR) for a fuller picture.

## Related in This Repo

- [EXTERNAL-RAG-RESOURCES.md](EXTERNAL-RAG-RESOURCES.md) — divesh-sse/RAGAS notebook + Streamlit demo
- [PYTHON-FOR-GENAI-CONCEPTS.md](PYTHON-FOR-GENAI-CONCEPTS.md)
- Interview bank: `08-projects-and-interview/INTERVIEW-QUESTIONS.md`
