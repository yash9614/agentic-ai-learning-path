# 03 — ReAct Agents & Tool Calling

## Core Concepts

**ReAct (Reason + Act)**  
The agent reasons about what to do, then acts (calls a tool), then observes the result and reasons again.

**Tool calling**  
The LLM decides which tool to call and with what arguments. The system executes the tool and returns the result.

## Key Notebooks

- `7-ReActAgents.ipynb` — Primary
- `6-chatbotswithmultipletools.ipynb`
- PDFs: `14-tool.pdf`, `15-ChatwithMultipletools.pdf`

## Interview Questions

1. Walk me through a ReAct agent loop.
2. How does tool calling work under the hood in LangChain/LangGraph?
3. How do you prevent infinite tool-calling loops?
4. What is the difference between a tool and a chain?
5. How would you add a new tool to an existing agent?

## Must-Do Project

Build a ReAct agent with at least two tools (e.g., search + calculator or Wikipedia). Add conditional routing so it stops when done.
