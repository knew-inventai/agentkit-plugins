# conventional-commits

根據 git diff 自動產生符合 [Conventional Commits](https://www.conventionalcommits.org/) 規範的 commit message。

## 安裝

```bash
/plugin install conventional-commits@agentkit-plugins
```

## 使用方式

先 `git add` 要提交的檔案，然後執行：

```
/commit
```

AI 會分析暫存的變更並產生：

```
feat(auth): implement JWT-based authentication

Add token generation and validation using jsonwebtoken.
Tokens expire after 24h and are stored in httpOnly cookies.

Closes #42
```

## Commit 類型

| type | 說明 |
|------|------|
| `feat` | 新功能 |
| `fix` | 修正 bug |
| `docs` | 文件變更 |
| `refactor` | 重構 |
| `test` | 新增/修改測試 |
| `chore` | 建置、依賴更新 |
| `perf` | 效能改善 |
| `ci` | CI 設定 |

## 為什麼用 Conventional Commits？

- 自動產生 CHANGELOG
- 語意化版本號判斷（feat → minor，fix → patch）
- 讓 git log 易讀易搜尋
