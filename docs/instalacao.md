# Instalação detalhada

Polícia Militar SP: Licenças do Corpo de Bombeiros (CLCB, AVCB E TAACB) é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_pm_sp_licenca_bombeiros`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_pm_sp_licenca_bombeiros` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_pm_sp_licenca_bombeiros` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_pm_sp_licenca_bombeiros` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.pm_sp_licenca_bombeiros` (ou `servers.pm_sp_licenca_bombeiros` no VS Code) do config do cliente e reinicie.
