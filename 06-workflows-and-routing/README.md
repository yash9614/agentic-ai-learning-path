# 06 — Workflows and Routing

## Core Concepts

Not everything needs full autonomy. Many production systems are **workflows** (predefined paths) with occasional agentic decisions.

**Routing** lets the system choose the right path:
- Vector store vs web search
- Different specialized agents
- Different tools based on intent

## Classic Workflow Patterns (from d-hackmt/langgraph-life)

- **Prompt chaining** — sequential nodes, each improving the previous output
- **Parallelization** — fan-out independent tasks, then join
- **Routing** — classifier node sends to specialized workers
- **Orchestrator-worker** — central orchestrator delegates to specialist subgraphs or tools
- **Evaluator-optimizer** — generate → critique → refine loop (with retry cap)

## Advanced Patterns (Telusko + sourangshupal)

- **Subgraphs**: Compose workflows by embedding one graph inside another. State is mapped explicitly when used as a node.
- **Parallel subgraphs** and output schemas.
- **Dynamic nodes and conditional edges**: Decide structure at runtime.
- **Commands**: `Command(update=..., goto=...)` for explicit control.
- **Send / map-reduce**: Fan-out work dynamically, then reduce.
- Graph as a tool: wrap a compiled workflow so an agent can invoke it.
- Multi-agent systems (supervisor or peer) — see sourangshupal notebook 09 and Telusko `Agents in Langgraph 21-11-2026` (programs 17–21: supervisor, handoffs, orchestrator-workers, deep agent).
- Final Project: Head Chef supervisor that routes to recipe (RAG), nutrition (MCP), and grocery (store) agents with per-user isolation.

## Key Source Materials

- Telusko: `Advance LangGraph 14-11-2026` and `(part - 2) 15-11-2026` (programs 24–42, agents project)
- Telusko: `Agents in Langgraph 21-11-2026/agents` (supervisor, handoffs, deep agent)
- Telusko: `Agentic AI Final Project 22-11-2026` (full multi-agent + RAG + MCP system)
- [d-hackmt/langgraph-life](https://github.com/d-hackmt/langgraph-life) folder `04-workflows`
- [sourangshupal/langraph-tutorials](https://github.com/sourangshupal/langraph-tutorials) notebooks 06, 08, 09
- See also `reference/EXTERNAL-LANGGRAPH-TUTORIALS.md`

## Interview Questions

1. Difference between a workflow and a fully autonomous agent?
2. How do you implement intent-based routing?
3. When would you prefer a router over a ReAct agent?
4. Explain how state flows when a subgraph is attached as a node vs invoked.
5. What is the difference between a static conditional edge and a dynamic one?
6. How would you implement a map-reduce style fan-out in LangGraph?
7. Walk through an orchestrator-worker pattern. When is it better than a pure ReAct loop?
8. How does an evaluator-optimizer loop differ from a simple retry?
9. How does a multi-agent supervisor (e.g. Head Chef) differ from peer handoffs?
10. How do you isolate specialist agents so they only see the request text and their own tools?

## Must-Do

Build a parent graph that invokes a subgraph (or uses it as a node) for one step, then add a dynamic conditional edge based on state. Implement at least one classic pattern (orchestrator-worker or evaluator-optimizer). Optionally study the Meal Planner Final Project for a production-style supervisor.
