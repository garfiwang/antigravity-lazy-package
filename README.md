# AntiGravity 安裝懶人包 (Antigravity Lazy Package)

> **版本**：v2.0 (2026-06-08)  
> **適用平台**：AntiGravity / Claude Code 等支援自訂技能 (Skills) 之 AI Agent 助理  
> **維護者**：Rich Wang (問大師家族辦公室)

這是一份專為 **Rich** 設計的 **AntiGravity 安裝懶人包**。本儲存庫整合了您目前所有安裝過且驗證完成的 **19 個自訂技能 (Custom Skills)**，方便您在不同的專案環境中一鍵部署與快速連接。

---

## 🌟 包含的 19 個自訂技能一覽

| 編號 | 技能名稱 (Skill Name) | 主要功能說明 (Key Features) |
| :--- | :--- | :--- |
| **01** | [antigravity-notebooklm](skills/antigravity-notebooklm) | 整合 NotebookLM MCP，快速查詢您的個人知識庫。 |
| **02** | [antigravity-github](skills/antigravity-github) | 快速登入與設定 GitHub CLI 安全提交環境。 |
| **03** | [antigravity-firebase](skills/antigravity-firebase) | 連接 Firebase MCP，管理專案、讀寫 Firestore 資料庫。 |
| **04** | [antigravity-draw](skills/antigravity-draw) | AI 生圖指引規範（包含尺寸、風格與提示詞結構化模版）。 |
| **05** | [antigravity-workflow](skills/antigravity-workflow) | 標準化「開工、收工、新專案初始化」工作流，保障代碼提交安全。 |
| **06** | [antigravity-obsidian](skills/antigravity-obsidian) | 連接 Obsidian 知識管理庫 (MCPVault)，同步專案駕駛艙。 |
| **07** | [fb-long-post](skills/fb-long-post) | 撰寫具有高流量、戲劇張力與問大師品牌風格的 FB 長文。 |
| **08** | [html-slide-builder](skills/html-slide-builder) | 給定教材後自動生成 Reveal.js HTML 互動簡報並部署至 GitHub Pages。 |
| **09** | [image-prompt-wizard](skills/image-prompt-wizard) | 引導式問答生成 Midjourney / DALL-E 等英文圖片 Prompt 嚮導。 |
| **10** | [morning-briefing](skills/morning-briefing) | 早晨日報技能：查詢 Gmail、Google Calendar、Notion 產出美觀的日報 HTML。 |
| **11** | [newspaper-pptx](skills/newspaper-pptx) | 將新聞文章排版成《經濟日報》風格的單頁 PPTX 簡報。 |
| **12** | [notion-inspiration-box](skills/notion-inspiration-box) | 將您的臨時靈感與資訊快速儲存至 Notion 靈感盒資料庫。 |
| **13** | [notion-note](skills/notion-note) | 將任意文章、長筆記或思考新增到 Rich 的 Notion Note 資料庫。 |
| **14** | [pptx-legal-slide](skills/pptx-legal-slide) | 問大師家族辦公室專屬「簡報法規版」單頁 PPTX 投影片製作。 |
| **15** | [storytelling-7steps](skills/storytelling-7steps) | 基於「故事創作七步法」自動撰寫高感染力的故事與教學案例。 |
| **16** | [sync-inspiration](skills/sync-inspiration) | 一鍵同步瀏覽器或手機端的靈感 Clippings 至 Notion。 |
| **17** | [threads-post](skills/threads-post) | 生成適合 Threads 平台的每日理財與信託規劃短脆文。 |
| **18** | [weekly-schedule-report](skills/weekly-schedule-report) | 查詢 Calendar 與 Notion 自動產生每週進度報告網頁。 |
| **19** | [wendashi-pptx](skills/wendashi-pptx) | 問大師家族辦公室（Wendashi Family Office）品牌簡報製作。 |

---

## 🛠 安裝與使用方式

### 方式一：交給 AI 助理自動安裝（推薦）
在您的新專案中，直接把此 GitHub 儲存庫網址提供給 AntiGravity 或 AI 助理，並輸入：
```text
這是我的 Antigravity 懶人包儲存庫：
https://github.com/garfiwang/antigravity-lazy-package
請讀取這個 repo 的 SKILL.md，幫我安裝我所指定的技能。
```
AI 助理會讀取 `SKILL.md` 的引導流程，列出所有 19 個技能並依據您的選擇自動複製對應檔案到專案的 `.agents/skills/` 目錄下。

### 方式二：手動複製安裝
您可以直接下載本儲存庫，並將 `skills/` 底下對應的技能資料夾，複製到您專案根目錄的 `.agents/skills/` 底下。
例如：
```bash
# 建立 skills 目錄
mkdir -p .agents/skills/

# 複製 wendashi-pptx 技能到您的專案中
cp -R /path/to/antigravity-lazy-package/skills/wendashi-pptx .agents/skills/
```

---

## 🛡 安全與隱私規則 (Do's & Don'ts)

為了保護您的帳戶與敏感資料，請務必遵守以下安全規範：
- **禁止提交敏感 Key**：不要將 API Key、GitHub Token、Firebase Admin SDK 憑證寫入任何 Markdown 或程式碼中。
- **禁止提交個人清單**：請勿將 NotebookLM 匯出的 `notebooks.json` 或私人的筆記本 ID 清單提交到公開的 GitHub 上。
- **排除個人敏感產物**：本機產出的圖片、暫存測試 App、個人筆記等，均已被列入 `.gitignore` 排除，請保持此設定。
- **精準 Commit**：在收工提交代碼時，請使用 `git status` 與 `git diff` 仔細確認，只 Stage 本次相關檔案，切勿使用 `git add .` 無差別提交。
