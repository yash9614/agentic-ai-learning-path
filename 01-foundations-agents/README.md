# 01 — Foundations: Agents vs Agentic AI

## Core Concepts

**AI Agent**  
A system that can perceive, reason, and take actions toward a goal. Often uses tools.

**Agentic AI**  
Systems that exhibit agency: planning, multi-step reasoning, tool use, self-correction, memory, and collaboration. Goes beyond single-turn generation.

**Key distinction**  
- Generative AI = produce content  
- Agentic AI = decide *what to do* next, act, observe, and iterate

**The agent loop**  
think → act (tool or subgraph) → observe → think again  
(until a stop condition, step limit, or human interrupt)

## Course Mapping (Telusko)

- Early sessions: `Calling Your First LLM`, `Python Gaps for AI`, `Data Modeling with Pydantic`
- Agent mindset appears throughout the LangGraph and agents projects

## Transformer Foundations (for deeper understanding)

Before advanced agents, strengthen Transformer intuition:
- **sunnysavita10/Full-Stack-GenAI-Bootcamp-1.0** → `Class-09-19-Apr-Transformer-Intution` (handwritten + Notion notes PDFs)
- Continue with Class-10 and later self-attention / multi-head classes in the same bootcamp.

See full class mapping: [reference/SUNNYSAVITA-FULLSTACK-GENAI-BOOTCAMP.md](reference/SUNNYSAVITA-FULLSTACK-GENAI-BOOTCAMP.md)

## What to Study

- PDF: `1-+AI+agents+vs+agentic+AI.pdf` (in original dump)
- PDF: `18-Agents.pdf`
- Understand the difference between a simple chain and an agent loop.

**Source materials:**  
Original repo: [D-Downloads-sagenic-ri-btcamp-with-alngjraph-and-raghen](https://github.com/yash9614/D-Downloads-sagenic-ri-btcamp-with-alngjraph-and-raghen)

## Interview Questions

1. What is the difference between an AI agent and Agentic AI?
2. Explain the ReAct pattern in simple terms.
3. Why do agents need tools?
4. What are the main components of a modern agent (brain, memory, tools, planning)?
5. When would you use a simple chain vs a full agent?
6. What stops an agent from running forever?
7. In one sentence, what problem does self-attention solve that RNNs struggled with?

## Must-Learn Takeaway

Agents are not magic. They are loops: think → act → observe → think again, with explicit control over when to stop or ask a human. Strong Transformer intuition makes the "brain" of the agent clearer.
