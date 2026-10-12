# 02 — LangGraph Basics

## Core Concepts

LangGraph models agent workflows as **state graphs**:

- **State**: Shared data (messages, intermediate results) that flows through the graph.
- **Nodes**: Functions that do work (call LLM, call tool, update state).
- **Edges**: Define the flow (normal or conditional).
- **Conditional edges**: Route based on state (e.g., if tool call needed, go to tools node).

This is what enables cycles, branching, and persistent agent behavior.

## Key Notebooks (from original dump)

- `1-simplegraph.ipynb` — Start here
- `5-ChainsLangGraph.ipynb`
- `3-DataclassStateSchema.ipynb` — State schemas
- Folder: `3-Debugging` (LangGraph debugging)

## Interview Questions

1. Why use LangGraph instead of a simple LangChain chain?
2. What is a StateGraph? How does state flow?
3. Explain nodes vs edges. What is a conditional edge?
4. How do you handle cycles in LangGraph?
5. Difference between TypedDict, dataclass, and Pydantic for state?

## Must-Do

Build a tiny graph with 2–3 nodes and a conditional edge. Understand the execution flow.
