# 02 — LangGraph Basics

## Core Concepts

LangGraph models agent workflows as **state graphs**:

- **State**: Shared data (messages, intermediate results) that flows through the graph. One Pydantic model (or TypedDict) per graph.
- **Nodes**: Functions that do work (call LLM, call tool, update state). A node returns a partial update.
- **Edges**: Define the flow (normal or conditional).
- **Conditional edges**: Route based on state (e.g., if tool call needed, go to tools node).
- **Parallel nodes**: Multiple edges out of one node; join waits for all branches.
- **Loops**: Conditional edge pointing backwards, with a retry counter so it cannot run forever.

This is what enables cycles, branching, and persistent agent behavior.

## Advanced Concepts (Telusko + external tutorials)

- **Reducers**: When parallel nodes write the same field, use `Annotated[type, reducer]` (e.g. `operator.add` or custom function).
- **Subgraphs**: Attach one graph inside another (as a node or via `invoke`).
- **Memory & Checkpointers**: `InMemorySaver` or `SqliteSaver`. One checkpoint per step. Parent and subgraph can share or keep separate memory.
- **Commands**: `Command(update=..., goto=..., resume=...)` for control flow and resuming interrupts.
- **Send / Map-Reduce**: Fan-out work dynamically with `Send`.
- **Dynamic nodes & edges**: Create nodes or conditional edges at runtime.
- **Tools inside graphs**: Bind tools, use `ToolNode`, interrupt *inside* a tool for approval.
- **Long-term memory** and functional API patterns (see sourangshupal tutorials).
- **Workflow patterns**: prompt chaining, parallelization, routing, orchestrator-worker, evaluator-optimizer (see d-hackmt/langgraph-life).

## Key Source Materials

- Telusko course folders: `Getting Started with LangGraph 17-10-2026` through `Advance LangGraph (part - 2) 15-11-2026`
- Progressive tutorials: [sourangshupal/langraph-tutorials](https://github.com/sourangshupal/langraph-tutorials) (10 notebooks: intro → conditional routing → tools → persistence → HITL → parallel/subgraphs → production → Command/functional API/long-term memory → multi-agent → testing/observability)
- Hands-on notebooks + diagrams: [d-hackmt/langgraph-life](https://github.com/d-hackmt/langgraph-life) (basics, components, debugging/Studio, workflows, HITL, RAG, multimodal)
- Original dump notebooks: `1-simplegraph.ipynb`, state schema examples

## Interview Questions

1. Why use LangGraph instead of a simple LangChain chain?
2. What is a StateGraph? How does state flow?
3. Explain nodes vs edges. What is a conditional edge?
4. How do you handle cycles in LangGraph? Why a retry counter?
5. What happens when two parallel nodes write the same field? How do reducers work?
6. Difference between attaching a subgraph as a node vs calling it with invoke?
7. How does checkpointing enable human-in-the-loop and multi-day runs?
8. What is the difference between `Command(goto=...)` and a normal edge?
9. Name three common workflow patterns you can implement with LangGraph (chaining, parallel, orchestrator-worker).

## Must-Do

Build a graph with parallel nodes + a reducer, then add a subgraph with its own memory, and finally add one interrupt that survives a process restart (SqliteSaver). Compare with the progressive notebooks in the two tutorial repos above.
