---
name: antigravity-lazy-package
description: AntiGravity 安裝懶人包 — 一鍵管理與引導安裝您目前的所有 22 個自訂技能。說「安裝 Antigravity 懶人包」「載入所有技能」時載入。
---

# AntiGravity 安裝懶人包 — AI Agent 自動安裝入口

本懶人包包含了您目前所安裝過的所有自訂技能（共 22 個）。您可以隨時將此儲存庫作為您在不同專案、不同環境的 AI Agent 技能基底。

## 技能清單與說明

| 編號 | 技能名稱 (Skill Name) | 說明 (Description) | 目錄路徑 |
| :--- | :--- | :--- | :--- |
| **01** | `antigravity-notebooklm` | 在 AntiGravity 連接 NotebookLM MCP | `skills/antigravity-notebooklm` |
| **02** | `antigravity-github` | 在 AntiGravity 連接 GitHub CLI | `skills/antigravity-github` |
| **03** | `antigravity-firebase` | 在 AntiGravity 連接 Firebase MCP | `skills/antigravity-firebase` |
| **04** | `antigravity-draw` | AntiGravity 生圖指引，規範畫圖/產生圖片提示詞 | `skills/antigravity-draw` |
| **05** | `antigravity-workflow` | AntiGravity 開工/收工/新專案初始化流程 | `skills/antigravity-workflow` |
| **06** | `antigravity-obsidian` | 在 AntiGravity 連接 Obsidian MCP (MCPVault) | `skills/antigravity-obsidian` |
| **07** | `fb-long-post` | 專為 Rich（信託規劃專家）撰寫高流量 FB 長文與文案優化 | `skills/fb-long-post` |
| **08** | `html-slide-builder` | 根據教材自動生成 Reveal.js HTML 互動簡報並部署 | `skills/html-slide-builder` |
| **09** | `image-prompt-wizard` | AI 圖片 Prompt 生成嚮導（引導式生成中/英文雙語 Prompt） | `skills/image-prompt-wizard` |
| **10** | `morning` | 早晨日報技能：查詢 Gmail、Google Calendar、Notion 產出日報網頁 | `skills/morning-briefing` |
| **11** | `newspaper-pptx` | 新聞排版技能：將新聞排版成經濟日報報紙風格單頁 PPTX | `skills/newspaper-pptx` |
| **12** | `notion-inspiration-box` | 快速將靈感、想法與資訊儲存到 Notion 靈感收集資料盒 | `skills/notion-inspiration-box` |
| **13** | `notion-note` | 將文章、筆記或想法新增到 Rich 的 Notion Note 資料庫 | `skills/notion-note` |
| **14** | `pptx-legal-slide` | 製作問大師家族辦公室「簡報法規版」單頁 PPTX 投影片 | `skills/pptx-legal-slide` |
| **15** | `storytelling-7steps` | 用「故事創作七步法」寫故事、強化草稿與案例設計 | `skills/storytelling-7steps` |
| **16** | `sync-inspiration` | 同步瀏覽器/手機靈感盒 Clippings 到 Notion | `skills/sync-inspiration` |
| **17** | `threads-post` | 為 Rich 生成適合 Threads 的每日短文/脆文 | `skills/threads-post` |
| **18** | `weekly-report` | 產生每週進度報告 HTML（整合 Google Calendar & Notion） | `skills/weekly-schedule-report` |
| **19** | `wendashi-pptx` | 製作問大師家族辦公室（Wendashi Family Office）品牌簡報 | `skills/wendashi-pptx` |
| **20** | `startup` | 開工自動同步流程，讀取 Obsidian 狀態與 Git 狀態（只讀不寫）。 | `skills/startup` |
| **21** | `shutdown` | 收工自動同步流程，專案 Git 同步、Chezmoi 同步與安全檢查。 | `skills/shutdown` |
| **22** | `project-init` | 新專案初始化流程，自動建立專案文件、Git 初始化與 GitHub 私有 Repo 建立。 | `skills/project-init` |

---

## 自動安裝與更新指引

當使用者要求安裝或更新自訂技能時，請依照下列步驟執行：

### 步驟一：讓使用者選擇
向使用者列出上表，詢問使用者要安裝「**全部技能**」或是「**指定編號組合**（例如：01, 05, 08）」。

### 步驟二：執行安裝
若是安裝選定的技能，請將該技能目錄下的整個資料夾（包含 `SKILL.md` 及所有關聯的 `scripts` 或 `references` 子目錄）複製到目前專案的 `.agents/skills/` 目錄中。

例如安裝 `html-slide-builder` 到專案：
```bash
mkdir -p .agents/skills/
cp -R <懶人包路徑>/skills/html-slide-builder .agents/skills/
```

### 步驟三：回報狀態
回報每個技能的複製安裝狀態（例如：`✅ html-slide-builder 安裝成功`），並提示使用者重新載入或重啟 Agent 以加載新技能。
