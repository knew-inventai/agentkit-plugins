---
description: 根據目前的 git diff 產生符合 Conventional Commits 規範的 commit message
allowed-tools: Bash(git diff:*)
---

請執行 `git diff --staged` 取得目前暫存的變更，然後根據以下規則產生一個 commit message：

**格式：**
```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

**type 選項：**
- feat：新功能
- fix：修正 bug
- docs：文件變更
- style：格式調整（不影響邏輯）
- refactor：重構（非新功能也非 bug 修正）
- test：新增或修改測試
- chore：建置流程、依賴更新等
- perf：效能改善
- ci：CI 設定變更

**規則：**
- description 使用英文、祈使句、小寫開頭、不加句號
- scope 為受影響的模組名稱（可省略）
- 如有 breaking change，在 footer 加 `BREAKING CHANGE: 說明`
- body 說明「為什麼」而非「做了什麼」

產生後請直接顯示完整的 commit message，讓使用者確認後可直接使用。
