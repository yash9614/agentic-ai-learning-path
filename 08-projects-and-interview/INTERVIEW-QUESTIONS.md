# Interview Question Bank — Agentic AI

## Foundational

1. Difference between Generative AI and Agentic AI?
2. What is an agent? What are its core components?
3. Explain the ReAct pattern with an example.
4. Why do we need frameworks like LangGraph?

## LangGraph Specific

5. What is a StateGraph?
6. How do conditional edges work?
7. How do you manage state in LangGraph?
8. How do you handle persistence and checkpoints?
9. What are common ways agents can fail in a graph?
10. What happens when parallel nodes write the same field? How do reducers work?
11. Difference between attaching a subgraph as a node vs calling it with invoke?
12. What is the difference between `Command(goto=...)` and a normal edge?
13. How does `Send` enable map-reduce style fan-out?
14. How do you create dynamic nodes or conditional edges?

## Tool Calling & RAG

15. How does tool calling work?
16. What is Agentic RAG? How is it different from standard RAG?
17. Explain Corrective RAG (CRAG) vs Self-RAG.
18. How do you evaluate an agentic system? (Name RAGAS metrics.)
19. How do you prevent infinite loops in agents?

## Multi-Agent & Frameworks

20. CrewAI sequential vs hierarchical?
21. What is a Deep Agent and when would you use it?
22. Difference between LangGraph, CrewAI, and Deep Agents?

## Production & Advanced

23. What is Human-in-the-Loop and when do you use it?
24. How do you handle two interrupts that fire in the same step?
25. Can an interrupt live inside a tool? When is that useful?
26. Why SQLite checkpointer over in-memory for production HITL?
27. What is MCP and why is it useful?
28. How would you add observability to an agent?
29. Difference between workflows and autonomous agents?
30. How do you control cost and latency in agent systems?
31. What guardrails would you put around a production agent?
32. How do you design least-privilege tools for a production agent (e.g., SQL + vector + API)?

## Project Streak Specific (Full-Stack Hybrid Patterns)

33. Explain the difference between calling tools directly vs exposing them via an MCP server. When would you choose each?
34. Walk through the request flow in the Travel Planning Agent when a user asks for today’s date and Kyoto tips (tool + RAG).
35. How does semantic routing work in the e-commerce assistant, and what are the trade-offs vs pure LLM classification?
36. Why use structured outputs (Pydantic + `parse`) instead of asking the model to return JSON and parsing it yourself?
37. What is the role of the dual path (Streamlit direct vs FastAPI + MCP) in project 00?
38. How would you make the Travel Planning Agent production-ready?

**Practice tip:** Answer out loud. Draw the graph. Explain trade-offs.

## External interview banks

- Full curated set in this ecosystem: [makan_m/learning-concepts/15-interview-questions.md](https://github.com/yash9614/makan_m/blob/main/learning-concepts/15-interview-questions.md)
- Project Streak analysis + questions: [makan_m/learning-concepts/sources/project-streak-notes.md](https://github.com/yash9614/makan_m/blob/main/learning-concepts/sources/project-streak-notes.md)
- Large AI Engineering cheat sheet (starred): [amitshekhariitbhu/ai-engineering-interview-questions](https://github.com/amitshekhariitbhu/ai-engineering-interview-questions) — covers LLM fundamentals, RAG, Agents, LLMOps, evaluation, system design, safety.
- See also `reference/STARRED-AND-FORKED-RESOURCES.md` for more project and tutorial sources.
