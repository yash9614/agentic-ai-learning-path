# 05 — Human-in-the-Loop (HITL)

## Core Concepts

Agents that can pause and ask a human for approval before taking sensitive actions (sending email, making a purchase, deleting data, etc.).

LangGraph supports this via:
- `interrupt(...)` called inside a node or tool
- Checkpointer (`InMemorySaver` or `SqliteSaver`) + `thread_id`
- `Command(resume=value)` to continue
- Resume re-runs the interrupted node from the top — put side effects *after* the interrupt

## Patterns Covered in the Course

- Single-node interrupt
- Interrupts across multiple nodes (confirm → style → generate, or cancel)
- **Parallel interrupts** (manager + finance both pause in the same step; answer by interrupt id)
- Interrupt **inside a tool** (approval gate travels with the action, even over MCP)
- Durable checkpoints in SQLite: start today, finish tomorrow. Use `get_state(config).next` to detect pending runs.
- One checkpoint per step (not per invoke)

## Key Source Materials

- Telusko: `Types of Graphs (Part - 2) 31-10-2026`, `Types of Graphs (Part - 3) 01-11-2026`, `Types of Graphs (Part - 4) 07-11-2026` (programs 16–23, 29)
- Original: `1-Humanintheloop.ipynb`

## Interview Questions

1. Why is Human-in-the-Loop important for production agents?
2. How do you implement approval gates in LangGraph?
3. What is the role of checkpoints in HITL systems? Why SQLite over in-memory?
4. What happens when you resume an interrupt? Why must side effects come after it?
5. How do you handle two interrupts that fire in the same step?
6. Can an interrupt live inside a tool? When is that useful?

## Must-Do

Add an approval interrupt to a sensitive tool, then make the same graph survive a process restart using SqliteSaver and a thread_id.
