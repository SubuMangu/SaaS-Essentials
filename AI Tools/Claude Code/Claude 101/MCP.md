# MCP
- `/mcp`: to check the connect mcp servers and their status

## Commands to add custom mcp server in claude
1. **Through HTTP**
- HTTP servers are for remote services. These are hosted by the service provider and connect over the network.
```
claude mcp add --transport http [connector name] [connector link]
```

**Example**
```
claude mcp add --transport http linear-server https://mcp.linear.app/mcp
```

2. **Through Stdio**
- Stdio servers are for local processes that run on your machine.

```
claude mcp add transport stdio dev-utils -- python C:/Users/lewis/mcp-server/server.py
```

## Scopes of MCP Servers
MCP servers can be scoped in three ways:

1. **Local** — only available in the current project, just for you.
2. **User** — available across all your projects.
3. **Project** — uses a .mcp.json file that you check into version control so anyone on the codebase gets the exact same servers automatically.