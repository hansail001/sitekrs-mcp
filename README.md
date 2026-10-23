# SiteKrs MCP

## English

SiteKrs MCP lets AI clients discover SiteKrs static-site templates and open a chosen template directly in the SiteKrs visual editor. It is intentionally small: two anonymous tools, no source upload, and no OAuth/PAT.

- **Endpoint:** `https://sitekrs.ai-krs.com/api/mcp`
- **Transport:** Streamable HTTP (POST)
- **Authentication:** none
- **Tools:** `list_templates`, `create_site`
- **Website:** `https://sitekrs.ai-krs.com`
- **Privacy:** `https://sitekrs.ai-krs.com/docs/mcp/privacy/`
- **Contact:** `support@ai-krs.com`

### Listing copy

> SiteKrs — from 0 to a static website: zero learning curve, save 90% of your time, one-time payment, permanently maintenance-free. The SiteKrs MCP server only lists templates and returns editor links; to use your own source, import a folder/ZIP manually through the “Import Template” dialog on the SiteKrs homepage.

Short description for registry fields (≤100 characters):

> List SiteKrs templates and get editor links; import your own source on the SiteKrs homepage.

### What it does

`list_templates` returns the SiteKrs template catalog with IDs, names, categories and descriptions. `create_site` accepts a `template_id` and returns an editor URL such as `https://sitekrs.ai-krs.com/#/editor?template=html5up-aerial`.

The MCP server never receives, reads or uploads user source files. If you have your own HTML/CSS/JS project, open the SiteKrs homepage, click **Import Template**, and select a folder or ZIP. The existing import dialog supports multi-page projects and detects dynamic runtime content before importing.

### Client configuration

Cline / Cursor / generic Streamable HTTP client:

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

Example prompts:

- “List the SiteKrs templates in the portfolio category.”
- “Create a SiteKrs site from the html5up-aerial template and give me the editor link.”
- “Which SiteKrs template should I use for a one-page restaurant site?”

### Repository scope

This public repository contains listing metadata and documentation only. The SiteKrs application source is private and is not published here. The MCP endpoint is hosted by SiteKrs on Cloudflare Pages.

---

## 中文

SiteKrs MCP 让 AI 客户端发现 SiteKrs 的静态网站模板，并直接把选中的模板打开到 SiteKrs 可视化编辑器。它刻意保持很小：两个匿名工具，不接收源码，不需要 OAuth/PAT。

- **端点：** `https://sitekrs.ai-krs.com/api/mcp`
- **传输：** Streamable HTTP（POST）
- **鉴权：** 无
- **工具：** `list_templates`、`create_site`
- **网站：** `https://sitekrs.ai-krs.com`
- **隐私政策：** `https://sitekrs.ai-krs.com/docs/mcp/privacy/`
- **联系邮箱：** `support@ai-krs.com`

### 上架文案

> SiteKrs — 从 0 到静态网站，零门槛操作、节省90%时间、一次性付费、永久免维护。SiteKrs MCP 只展示模板并返回编辑器链接，自有源码可在SiteKrs首页「导入模版」用文件夹/ZIP 手动导入。

适合 Registry 字段的短描述（≤100 字符）：

> List SiteKrs templates and get editor links; import your own source on the SiteKrs homepage.

### 功能说明

`list_templates` 返回 SiteKrs 模板目录，包括模板 ID、名称、分类和说明。`create_site` 接收 `template_id`，返回类似 `https://sitekrs.ai-krs.com/#/editor?template=html5up-aerial` 的编辑器链接。

MCP 服务不接收、不读取、不上传用户源码。如果你有自己的 HTML/CSS/JS 项目，请打开 SiteKrs 首页，点击「导入模版」，选择文件夹或 ZIP。现有导入弹窗支持多页项目，并会在导入前检测运行时动态内容。

### 客户端配置

Cline / Cursor / 通用 Streamable HTTP 客户端：

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

示例提示词：

- “列出 SiteKrs 作品集分类下的模板。”
- “用 html5up-aerial 模板创建一个 SiteKrs 站点，并给我编辑器链接。”
- “做一个单页餐厅网站，推荐哪个 SiteKrs 模板？”

### 仓库范围

这个公开仓库只包含上架元数据和说明文档。SiteKrs 应用源码是私有的，不在这里发布。MCP 端点由 SiteKrs 托管在 Cloudflare Pages 上。
