# JUCESP: Busca de NIRE (pesquisa avançada)

### JUCESP: Busca de NIRE (pesquisa avançada) for Claude, ChatGPT and AI agents

Advanced company search at JUCESP by name, purpose, capital and address, returning the NIRE. Platform-hosted, no credentials, pay per query with prepaid credit.

- 📊 **1 tool**
- 🔒 **Read-only**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `JUCESP: Busca de NIRE (pesquisa avançada)`, URL `https://api.mcp.ai/p_jucesp_nire`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=jucesp_nire&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9qdWNlc3BfbmlyZSJ9)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=jucesp_nire&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_jucesp_nire%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_jucesp_nire
```

---

## 1 tool

| Tool | Description |
|---|---|
| `jucesp_nire_consultar` | Pesquisa avançada de empresas na JUCESP por razão social, objeto, capital, endereço e outros filtros, retornando o NIRE. |

---

## Pricing

See [docs/precos.md](docs/precos.md) (PT-BR).

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_jucesp_nire` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
