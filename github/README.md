# github（Official Plugin）

GitHub 官方 Plugin，透過 GitHub Copilot MCP 服務提供完整 GitHub API 整合：建立 issues、管理 PR、code review、搜尋 repos，直接在 Claude Code 中操作。

## 安裝

```bash
/plugin install github@agentkit-plugins
```

## 設定

安裝後需設定 GitHub Personal Access Token：

```bash
export GITHUB_PERSONAL_ACCESS_TOKEN=<your-token>
```

或加入 `.mcp.json`：

```json
{
  "github": {
    "type": "http",
    "url": "https://api.githubcopilot.com/mcp/",
    "headers": {
      "Authorization": "Bearer ${GITHUB_PERSONAL_ACCESS_TOKEN}"
    }
  }
}
```

## 取得 Token

1. 前往 https://github.com/settings/tokens
1. 建立 Fine-grained Token，選擇需要的 repository 權限
1. 將 token 填入 `GITHUB_PERSONAL_ACCESS_TOKEN`

## 可用功能

- 建立、更新、關閉 issues 與 PR
- Code review 與留言
- 搜尋 repositories、code、users
- 管理 branches 與 commits
- 讀寫檔案內容

## 來源

[anthropics/claude-plugins-official](https://github.com/anthropics/claude-plugins-official/tree/main/external_plugins/github)
