# 06 — Workflows and Routing

## Core Concepts

Not everything needs full autonomy. Many production systems are **workflows** (predefined paths) with occasional agentic decisions.

**Routing** lets the system choose the right path:
- Vector store vs web search
- Different specialized agents
- Different tools based on intent

## Advanced Patterns (Telusko Advance LangGraph)

- **Subgraphs**: Compose workflows by embedding one graph inside another. State is mapped explicitly when used as a node.
- **Parallel subgraphs** and output schemas.
- **Dynamic nodes and conditional edges**: Decide structure at runtime.
- **Commands**: `Command(update=..., goto=...)` for explicit control instead of (or in addition to) edges.
- **Send / map-reduce**: Fan-out work to many nodes dynamically, then reduce.
- Graph as a tool: wrap a compiled workflow so an agent can invoke it.

## Key Source Materials

- Telusko: `Advance LangGraph 14-11-2026` and `(part - 2) 15-11-2026` (programs 24–42, agents project)
- Original: `4- Workflows` folder, workflow PDFs

## Interview Questions

1. Difference between a workflow and a fully autonomous agent?
2. How do you implement intent-based routing?
3. When would you prefer a router over a ReAct agent?
4. Explain how state flows when a subgraph is attached as a node vs invoked.
5. What is the difference between a static conditional edge and a dynamic one?
6. How would you implement a map-reduce style fan-out in LangGraph?

## Must-Do

Build a parent graph that invokes a subgraph (or uses it as a node) for one step, then add a dynamic conditional edge based on state.
