# env-checker

掃描程式碼中的 hardcoded secrets 與敏感環境變數，在 commit 前提早發現安全問題。

## 安裝

```bash
/plugin install env-checker@agentkit-plugins
```

## 使用方式

```
/check-secrets
```

掃描目前工作目錄，找出：

- API keys（`sk-xxx`、`ghp_xxx`、`AKIA...` 等格式）
- 硬編碼密碼（`password=`、`passwd=` 等賦值）
- 私鑰與憑證（`BEGIN PRIVATE KEY` 等）
- URL 含認證資訊（`https://user:pass@host`）

每個問題都會標示檔案路徑、行號、風險等級，並建議改用環境變數的方式。

## 搭配 pre-commit 使用

可在 `.claude/settings.json` 的 hooks 中加入自動掃描：

```json
{
  "hooks": {
    "PreToolUse": [{
      "matcher": "Bash",
      "hooks": [{"type": "command", "command": "echo '記得執行 /check-secrets'"}]
    }]
  }
}
```
