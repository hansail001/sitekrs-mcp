# SiteKrs MCP — installation notes

## English

SiteKrs MCP is a remote Streamable HTTP server. Do not install a local package or ask for source files.

```json
{
  "mcpServers": {
    "sitekrs": {
      "type": "streamable-http",
      "url": "https://sitekrs.ai-krs.com/api/mcp"
    }
  }
}
```

- No authentication, API key, OAuth or PAT is required.
- Tools: `list_templates`, `create_site`.
- `list_templates` returns the template catalog.
- `create_site` returns a SiteKrs editor URL for a `template_id`.
- Own source code is imported manually on the SiteKrs homepage via **Import Template** → folder/ZIP. MCP never uploads source.
- Privacy: https://sitekrs.ai-krs.com/docs/mcp/privacy/
- Contact: support@ai-krs.com

## 中文

SiteKrs MCP 是远程 Streamable HTTP 服务，不需要安装本地包，也不需要提供源码文件。

```json
{
  "mcpServers": {
    "sitekrs": {
      "type": "streamable-http",
      "url": "https://sitekrs.ai-krs.com/api/mcp"
    }
  }
}
```

- 不需要鉴权、API Key、OAuth 或 PAT。
- 工具：`list_templates`、`create_site`。
- `list_templates` 返回模板目录。
- `create_site` 根据 `template_id` 返回 SiteKrs 编辑器链接。
- 自有源码请在 SiteKrs 首页通过「导入模版」→ 文件夹/ZIP 手动导入；MCP 不上传源码。
- 隐私政策：https://sitekrs.ai-krs.com/docs/mcp/privacy/
- 联系邮箱：support@ai-krs.com
