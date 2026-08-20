---
name: pm_sp_licenca_bombeiros-mcp
description: Skill da REST API do Polícia Militar SP: Licenças do Corpo de Bombeiros (CLCB, AVCB E TAACB) na MCP.AI: 1 endpoint em /api/pm_sp_licenca_bombeiros. Polícia Militar SP: Licenças do Corpo de Bombeiros (CLCB, AVCB E TAACB), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Polícia Militar SP: Licenças do Corpo de Bombeiros (CLCB, AVCB E TAACB) — REST API skill

Você tem acesso à **Polícia Militar SP: Licenças do Corpo de Bombeiros (CLCB, AVCB E TAACB)** REST API na MCP.AI.

> Polícia Militar SP: Licenças do Corpo de Bombeiros (CLCB, AVCB E TAACB), consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/pm_sp_licenca_bombeiros
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/pm_sp_licenca_bombeiros/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/pm_sp_licenca_bombeiros/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `pm_sp_licenca_bombeiros_consultar`

Polícia Militar SP: Licenças do Corpo de Bombeiros (CLCB, AVCB E TAACB), consulta em fonte oficial. _(POST /api/pm_sp_licenca_bombeiros/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `endereco` | string | Não | Parâmetro de consulta "endereco". |
| `municipio` | string | Não | Parâmetro de consulta "municipio". |
| `numero` | string | Não | Parâmetro de consulta "numero". |
| `bairro` | string | Não | Parâmetro de consulta "bairro". |
| `avcb` | string | Não | Parâmetro de consulta "avcb". |
| `clcb` | string | Não | Parâmetro de consulta "clcb". |
| `taacb` | string | Não | Parâmetro de consulta "taacb". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_pm_sp_licenca_bombeiros` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
