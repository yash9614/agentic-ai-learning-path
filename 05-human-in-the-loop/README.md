# 05 — Human-in-the-Loop (HITL)

## Core Concepts

Agents that can pause and ask a human for approval before taking sensitive actions (sending email, making a purchase, deleting data, etc.).

LangGraph supports this via:
- Interrupts
- Checkpoints / persistence
- Human nodes or conditional edges that wait for input

## Key Notebook

- `1-Humanintheloop.ipynb`

## Interview Questions

1. Why is Human-in-the-Loop important for production agents?
2. How do you implement approval gates in LangGraph?
3. What is the role of checkpoints in HITL systems?
4. Give an example of an action that should always require human approval.
5. How do you resume an agent after human input?

## Must-Do

Add an approval step to a tool-calling agent for at least one sensitive tool.
