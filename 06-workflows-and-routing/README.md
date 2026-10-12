# 06 — Workflows and Routing

## Core Concepts

Not everything needs full autonomy. Many production systems are **workflows** (predefined paths) with occasional agentic decisions.

**Routing** lets the system choose the right path:
- Vector store vs web search
- Different specialized agents
- Different tools based on intent

## Key Materials

- Folder: `4- Workflows`
- PDF: `24-28+Workflows.pdf`
- Notebooks involving chains + graphs

## Interview Questions

1. Difference between a workflow and a fully autonomous agent?
2. How do you implement intent-based routing?
3. When would you prefer a router over a ReAct agent?
4. Explain multi-agent collaboration patterns (supervisor, hierarchical, peer).

## Must-Do

Build a router that sends queries to either a vector store or an external search tool.
