# Instalação rápida

Polícia Militar SP: Licenças do Corpo de Bombeiros (CLCB, AVCB E TAACB) é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_pm_sp_licenca_bombeiros`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Polícia Militar SP: Licenças do Corpo de Bombeiros (CLCB, AVCB E TAACB)` / `https://api.mcp.ai/p_pm_sp_licenca_bombeiros`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "pm_sp_licenca_bombeiros": { "type": "http", "url": "https://api.mcp.ai/p_pm_sp_licenca_bombeiros" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=pm_sp_licenca_bombeiros&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9wbV9zcF9saWNlbmNhX2JvbWJlaXJvcyJ9)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "pm_sp_licenca_bombeiros": { "url": "https://api.mcp.ai/p_pm_sp_licenca_bombeiros" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=pm_sp_licenca_bombeiros&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_pm_sp_licenca_bombeiros%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "pm_sp_licenca_bombeiros": { "type": "http", "url": "https://api.mcp.ai/p_pm_sp_licenca_bombeiros" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_pm_sp_licenca_bombeiros
```

Dúvidas? [pm_sp_licenca_bombeiros@mcp.ai](mailto:pm_sp_licenca_bombeiros@mcp.ai)
