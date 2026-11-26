# 03 — ReAct Agents & Tool Calling

## Core Concepts

**ReAct (Reason + Act)**  
The agent reasons about what to do, then acts (calls a tool), then observes the result and reasons again.

**Tool calling**  
The LLM decides which tool to call and with what arguments. The system executes the tool and returns the result.

In LangGraph this is typically a model node (with `bind_tools`) + a `ToolNode` + a conditional edge that loops until the model stops calling tools.

## Course Coverage

- Basic ReAct loops
- Multiple tools
- Recursion / depth limits
- Graph used as a tool
- Agent with memory (checkpointer)
- Streaming modes (values, debug, checkpoint, tasks, messages)
- Human approval
- Plan-and-execute
- Multi-agent supervisor
- Agent handoffs
- Orchestrator-workers
- Deep agents

## Key Source Materials

- Telusko: `Advance LangGraph (part - 2) 15-11-2026/agents` (programs 1–9)
- Telusko: `Agents in Langgraph 21-11-2026/agents` (programs 1–21, including supervisor, handoffs, deep agent)
- Original dump: `7-ReActAgents.ipynb`, `6-chatbotswithmultipletools.ipynb`
- PDFs: `14-tool.pdf`, `15-ChatwithMultipletools.pdf`

## Interview Questions

1. Walk me through a ReAct agent loop.
2. How does tool calling work under the hood in LangChain/LangGraph?
3. How do you prevent infinite tool-calling loops?
4. What is the difference between a tool and a chain?
5. How would you add a new tool to an existing agent?
6. How do you stream intermediate steps or final tokens from an agent?
7. Difference between an agent that has its own checkpointer vs one that is stateless?
8. What is a multi-agent supervisor pattern? How do handoffs work?
9. When would you use a deep agent vs a simple ReAct agent?

## Must-Do Project

Build a ReAct agent with at least two tools. Add conditional routing so it stops when done. Optionally add memory, streaming, and a simple supervisor or handoff.
