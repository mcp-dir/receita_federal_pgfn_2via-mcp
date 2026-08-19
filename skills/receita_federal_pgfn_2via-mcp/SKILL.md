---
name: receita_federal_pgfn_2via-mcp
description: Skill da REST API do Receita Federal: PGFN (CND Federal) - Segunda Via na MCP.AI: 1 endpoint em /api/receita_federal_pgfn_2via. Receita Federal: PGFN (CND Federal) - Segunda Via, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Receita Federal: PGFN (CND Federal) - Segunda Via — REST API skill

Você tem acesso à **Receita Federal: PGFN (CND Federal) - Segunda Via** REST API na MCP.AI.

> Receita Federal: PGFN (CND Federal) - Segunda Via, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/receita_federal_pgfn_2via
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
curl -X POST https://api.mcp.ai/api/receita_federal_pgfn_2via/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/receita_federal_pgfn_2via/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `receita_federal_pgfn_2via_consultar`

Receita Federal: PGFN (CND Federal) - Segunda Via, consulta em fonte oficial. _(POST /api/receita_federal_pgfn_2via/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `birthdate` | string | Não | Parâmetro de consulta "birthdate". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_receita_federal_pgfn_2via` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
