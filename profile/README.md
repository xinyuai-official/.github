<div align="center">
  <img src="https://avatars.githubusercontent.com/u/360419940?v=4" alt="XinYu AI Logo" width="76" style="border-radius: 18px;" />
  <h2>XinYu AI · 心宇 AI</h2>
  <p><strong>One canvas, from spark to final cut.</strong><br/>一块画布，从灵感到成片 —— 面向创作者与 AI Agent 的原生多模态创作平台</p>

  <p>
    <a href="https://xinyuai.app"><img src="https://img.shields.io/badge/Studio-xinyuai.app-A3E635?style=flat-square&labelColor=111111" alt="Website" /></a>
    <a href="https://www.npmjs.com/package/@xinyuai/cli"><img src="https://img.shields.io/npm/v/@xinyuai/cli?style=flat-square&label=%40xinyuai%2Fcli&color=A3E635&labelColor=111111" alt="@xinyuai/cli" /></a>
    <a href="https://www.npmjs.com/package/@xinyuai/mcp-server"><img src="https://img.shields.io/npm/v/@xinyuai/mcp-server?style=flat-square&label=%40xinyuai%2Fmcp-server&color=A3E635&labelColor=111111" alt="@xinyuai/mcp-server" /></a>
    <a href="https://github.com/xinyuai-official/xinyu-skills"><img src="https://img.shields.io/badge/Agent_Skill-xinyu-38BDF8?style=flat-square&labelColor=111111" alt="Agent Skill" /></a>
  </p>

  <p>
    <a href="https://xinyuai.app">Website</a> ·
    <a href="https://xinyuai.app/en/cli">CLI Docs</a> ·
    <a href="https://xinyuai.app/en/mcp">MCP Docs</a> ·
    <a href="https://github.com/xinyuai-official/xinyu-skills">Agent Skills</a> ·
    <a href="https://xinyuai.app/zh">中文官网</a>
  </p>
</div>

---

### What We Build

**XinYu AI ([xinyuai.app](https://xinyuai.app))** brings storyboard breakdown, batch image generation, layer decomposition, cinema camera/lighting controls, and 4K video rendering onto **a single visual node canvas** — backed by one shared, non-expiring credit balance (**Xins / 心点**):

- **Frontier Multimodal Models**: **Seedance 2.5** (native 4K, up to 30s single-take, 480p draft → 1080p final), **Seedance 2.0** (image + video + audio multimodal references), **Kling 4.0 & O3**, **Wan 3.0**, **Nano Banana Pro**, **GPT Image 2.6**, **SeeDream 5.0 Pro**, **ElevenLabs**, and **Seed Audio**.
- **Agent-Native Tooling**: Every capability on the web canvas is exposed cleanly to terminals, CI pipelines, and AI coding agents via `@xinyuai/cli` (`--json` stdout + async job recovery) and `@xinyuai/mcp-server` (36+ structured MCP tools).

---

### Quick Start for AI Agents & Developers

```bash
# 1. Install the official Agent Skill (Claude Code, Cursor, Antigravity, Codex, OpenClaw)
npx skills add xinyuai-official/xinyu-skills --skill xinyu -g -y

# 2. Install the CLI (includes `xinyu` + built-in `xinyu mcp`)
npm install -g @xinyuai/cli
xinyu login --key xys_live_xxxx
xinyu balance --json
```

Or attach directly via **MCP** (`~/.gemini/config/mcp_config.json`, `.cursor/mcp.json`, or `claude_desktop_config.json`):

```json
{
  "mcpServers": {
    "xinyu": {
      "command": "npx",
      "args": ["-y", "@xinyuai/mcp-server"],
      "env": {
        "XINYU_API_KEY": "xys_live_xxxxxxxxxxxxxxxx"
      }
    }
  }
}
```

---

### Official Repositories & Packages

| Resource | Description |
| :--- | :--- |
| [**`xinyuai-official/xinyu-skills`**](https://github.com/xinyuai-official/xinyu-skills) | Official `SKILL.md` & MCP configuration templates for AI coding agents |
| [**`@xinyuai/cli`**](https://www.npmjs.com/package/@xinyuai/cli) | Command-line client (`xinyu`) for multimodal generation, asset upload & canvas node ops |
| [**`@xinyuai/mcp-server`**](https://www.npmjs.com/package/@xinyuai/mcp-server) | Model Context Protocol server exposing 36+ XinYu AI canvas & generation tools |
| [**`xinyuai.app`**](https://xinyuai.app) | Web & Desktop Studio (macOS & Windows) · Contact: `support@xinyuai.app` |
