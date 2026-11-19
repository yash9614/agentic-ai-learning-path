# 07 — MCP Integration with LangGraph

## Core Concepts

**Model Context Protocol (MCP)** is a standard way for agents to discover and call tools provided by external servers.

Benefits:
- Tools live outside the agent process
- Standardized interface
- Easier to share tools across agents and clients

Transports: stdio, streamable HTTP (SSE).

## Course Mapping (Telusko)

- `MCP (Part - 2) 13-09-2026`
- `MCP (Part -3) 19-09-2026`
- `MCP (Part - 4) 20-09-2026`
- `Building a Support App with MCP 11-10-2026`

These cover FastMCP servers/clients, streamable HTTP, and a full support-app example.

## Materials in This Ecosystem

- Folder `mcplanggraph` in the original agentic dump
- Full projects: [MCP_PROJECTS_oo3](https://github.com/yash9614/MCP_PROJECTS_oo3)  
  Contains servers, clients, SSE transport, multi-server support, LangChain MCP adapters, etc.

## Interview Questions

1. What is MCP and why does it matter for agents?
2. How does an agent discover tools from an MCP server?
3. Difference between embedding tools directly vs exposing them via MCP?
4. What transports does MCP support (stdio, streamable HTTP)?
5. How would you put an approval interrupt inside a tool that is served over MCP?

## Must-Do

Connect a LangGraph agent to at least one MCP server and call its tools. Optionally expose one of your own tools via FastMCP.
