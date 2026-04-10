# AI Skills

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)


> Skills 遵循 [Claude Code skill 規範](https://code.claude.com/docs/en/skills)（SKILL.md + scripts/），但概念不限定於特定框架。把它們想成你的 AI 真的會照著做的 checklist。

> **安全聲明：** 這些 skills 設計用於本地開發和受信任的內網環境。與外部服務互動的 skill（如 `searxng`）預設採用安全設定（TLS 驗證啟用），但不包含額外的認證機制。部署到敏感環境前請先檢閱各 skill 的設定。

## Skills

| Skill | 它到底幹嘛 |
|-------|----------|

| [repo-scan](repo-scan/) | 安裝之前先幫 GitHub repo 做安全掃描。靜態分析、依賴審計、供應鏈風險、Issues 漏洞回報、維護者健康度 — 因為 `npm install 不知名套件` 不該是一場賭博 |
| [job-scout](job-scout/) | 投履歷之前先把公司查清楚。薪資、評價、紅旗、財務狀況 |


## 安裝

拿你需要的，不需要的不用管：

**macOS / Linux：**
```bash

# 範例：安裝到 Claude Code（使用者層級）
cp -r kc_ai_skills/prep-repo ~/.claude/skills/

# 範例：安裝到 OpenClaw（workspace 層級）
cp -r kc_ai_skills/searxng ~/.openclaw/workspace/skills/
```

**Windows（PowerShell）：**
```powershell

# 範例：安裝到 Claude Code（使用者層級）
Copy-Item -Recurse prep-repo "$env:USERPROFILE\.claude\skills\"

# 範例：安裝到 OpenClaw（workspace 層級）
Copy-Item -Recurse searxng "$env:USERPROFILE\.openclaw\workspace\skills\"
```


> **其他客戶端：** 每個 SKILL.md 都是獨立的 markdown 指令文件。直接複製貼上到任何 AI 對話、system prompt 或自訂指令欄位就能用。不用裝 SDK，不用 API key — 就是複製貼上。

## Skill 結構

每個 skill 遵循一個簡單到不行的規範。會寫 markdown 就會寫 skill：

```
skill-name/
├── SKILL.md          # Frontmatter（name, description, version）+ 指令
└── scripts/          # 可執行腳本（選用）
    └── script.py
```

## References

- [kc_ai_skills](https://github.com/KerberosClaw/kc_ai_skills/tree/main)
