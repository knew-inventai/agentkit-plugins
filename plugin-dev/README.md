# plugin-dev

Anthropic 官方的 Claude Code Plugin 開發工具包，提供七個專業 Skill 協助你從零開始開發高品質的 Claude Code plugin。

## 安裝

```bash
/plugin install plugin-dev@claude-code-marketplace
```

## 涵蓋主題

| Skill | 說明 |
|-------|------|
| Hook Development | PreToolUse / PostToolUse 等事件驅動自動化 |
| MCP Integration | 整合外部 API、資料庫、服務 |
| Plugin Structure | plugin.json manifest 與目錄結構 |
| Plugin Settings | `.claude/plugin-name.local.md` 設定模式 |
| Command Development | Slash command 設計與 frontmatter |
| Agent Development | 自主 agent 建立與 AI 輔助生成 |
| Skill Development | 為 plugin 建立 skill（本 Skill 本身即範例） |

## 使用方式

安裝後詢問任何 plugin 開發相關問題，對應的 Skill 會自動觸發：

- 「幫我建立一個 PreToolUse hook 來驗證檔案寫入」
- 「如何在 plugin 中設定 MCP server？」
- 「我想加入一個 /check slash command」

## 來源

[anthropics/claude-code/plugins/plugin-dev](https://github.com/anthropics/claude-code/tree/main/plugins/plugin-dev)
