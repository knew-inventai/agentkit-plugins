---
description: 掃描目前工作目錄，找出可能的 hardcoded secrets 或 API keys
---

請掃描目前專案的程式碼，找出所有可能的 hardcoded secrets，包含：

1. API keys（格式如 sk-xxx、ghp_xxx、AKIA 開頭等）
2. 密碼（password=、passwd= 等賦值）
3. 私鑰或憑證（BEGIN PRIVATE KEY 等）
4. 硬編碼的 URL 含認證資訊（https://user:pass@...）

對每個發現的問題：
- 指出檔案路徑與行號
- 說明風險等級（高/中/低）
- 建議改用環境變數的方式

忽略 .env.example、測試用假資料（如 test-key-xxx）、以及 node_modules/。
