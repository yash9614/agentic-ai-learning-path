# 07 — MCP Integration with LangGraph

## Core Concepts

**Model Context Protocol (MCP)** is a standard way for agents to discover and call tools provided by external servers.

Benefits:
- Tools live outside the agent process
- Standardized interface
- Easier to share tools across agents and clients

## Materials in This Ecosystem

- Folder `mcplanggraph` in the original agentic dump
- Full projects: [MCP_PROJECTS_oo3](https://github.com/yash9614/MCP_PROJECTS_oo3)  
  Contains servers, clients, SSE transport, multi-server support, LangChain MCP adapters, etc.

## Interview Questions

1. What is MCP and why does it matter for agents?
2. How does an agent discover tools from an MCP server?
3. Difference between embedding tools directly vs exposing them via MCP?
4. What transports does MCP support (stdio, SSE, etc.)?

## Must-Do

Connect a LangGraph agent to at least one MCP server and call its tools.
