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

## Advanced Concepts (from Telusko Advance LangGraph sessions)

- **Reducers**: When parallel nodes write the same field, use `Annotated[type, reducer]` (e.g. `operator.add` or custom function). Reducer only sees its own field.
- **Subgraphs**: Attach one graph inside another (as a node or via `invoke`). State mapping differs by attachment style. Support parallel subgraphs, xray inspection, and HITL inside subgraphs.
- **Memory & Checkpointers**: `InMemorySaver` or `SqliteSaver`. One checkpoint per step. `get_state(config).next` tells you if a run is waiting. Parent and subgraph can share or keep separate memory.
- **Commands**: `Command(update=..., goto=..., resume=...)` for control flow, including resume after interrupt.
- **Send / Map-Reduce**: Fan-out work dynamically with `Send`.
- **Dynamic nodes & edges**: Create nodes or conditional edges at runtime.
- **Tools inside graphs**: Bind tools, use `ToolNode`, interrupt *inside* a tool for approval.

## Key Source Materials

- Telusko course folders: `Getting Started with LangGraph 17-10-2026`, `Types of Graphs 18-10-2026`, `Types of Graphs (Part - 2/3/4)`, `Advance LangGraph 14-11-2026`, `Advance LangGraph (part - 2) 15-11-2026`
- Programs 1–42 covering the progression above
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

## Must-Do

Build a graph with parallel nodes + a reducer, then add a subgraph with its own memory, and finally add one interrupt that survives a process restart (SqliteSaver).
