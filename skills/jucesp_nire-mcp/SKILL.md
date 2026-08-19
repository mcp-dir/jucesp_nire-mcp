---
name: jucesp_nire-mcp
description: Skill da REST API do JUCESP: Busca de NIRE (pesquisa avançada) na MCP.AI: 1 endpoint em /api/jucesp_nire. Pesquisa avançada de empresas na JUCESP por razão social, objeto, capital, endereço e outros filtros, retornando o NIRE. Hospedado pela plataforma, sem credenciais, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# JUCESP: Busca de NIRE (pesquisa avançada) — REST API skill

Você tem acesso à **JUCESP: Busca de NIRE (pesquisa avançada)** REST API na MCP.AI.

> Pesquisa avançada de empresas na JUCESP por razão social, objeto, capital, endereço e outros filtros, retornando o NIRE. Hospedado pela plataforma, sem credenciais, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/jucesp_nire
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
curl -X POST https://api.mcp.ai/api/jucesp_nire/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/jucesp_nire/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `jucesp_nire_consultar`

Pesquisa avançada de empresas na JUCESP por razão social, objeto, capital, endereço e outros filtros, retornando o NIRE. _(POST /api/jucesp_nire/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `razao_social` | string | Não | Parâmetro de consulta "razao_social". |
| `objeto` | string | Não | Parâmetro de consulta "objeto". |
| `capital_minimo` | string | Não | Parâmetro de consulta "capital_minimo". |
| `capital_maximo` | string | Não | Parâmetro de consulta "capital_maximo". |
| `abertura_inicio` | string | Não | Parâmetro de consulta "abertura_inicio". |
| `abertura_fim` | string | Não | Parâmetro de consulta "abertura_fim". |
| `dissolucao_inicio` | string | Não | Parâmetro de consulta "dissolucao_inicio". |
| `dissolucao_fim` | string | Não | Parâmetro de consulta "dissolucao_fim". |
| `logradouro` | string | Não | Parâmetro de consulta "logradouro". |
| `cep` | string | Não | Parâmetro de consulta "cep". |
| `bairro` | string | Não | Parâmetro de consulta "bairro". |
| `municipio` | string | Não | Parâmetro de consulta "municipio". |
| `uf` | string | Não | Parâmetro de consulta "uf". |
| `tipo_empresa` | string | Não | Parâmetro de consulta "tipo_empresa". |
| `inclui_inativas` | string | Não | Parâmetro de consulta "inclui_inativas". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_jucesp_nire` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
