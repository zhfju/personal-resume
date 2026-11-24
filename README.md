# 周鉦浤 — 個人簡歷網站 (Personal Portfolio)

> **Keep it simple, keep it real.**

- **GitHub Pages 線上預覽**：https://zhfju.github.io/personal-resume/
- **個人主站**：https://zh-web.onrender.com/#home
- **聯絡信箱**：fjuzhou@gmail.com

---

## 📌 專案簡介

本專案為單頁式響應式個人簡歷網站（Single Page Portfolio），採用 **Editorial 雜誌專刊雙欄釘選風格** 設計：桌面版左側固定個人識別、章節導覽與聯絡連結，右側依序展開自我介紹、技能工具箱、學習經歷時間軸與獨立開發作品實機影片；行動版（`< 600px`）自動切換為頂部懸浮導覽與單欄舒適閱讀版面。

### 網站架構與互動特色

1. **個人資訊區塊**：整合個人頭像、系級（醫資一）、核心理念，以及 Email 一鍵複製回饋按鈕、個人主站與 GitHub 連結。
2. **技能與工具箱（標籤雲＋分類篩選）**：將橫跨前端／後端語言、雲端部署、自動化腳本、知識管理與運動剪輯共 16 項技能精簡命名，搭配專屬向量圖示（SVG Icon）與四大分類即時篩選器。
3. **學習與經歷時間軸**：記錄從國中程式社（Arduino、micro:bit、3D 列印建模）、高中前端探索與 Java／羽球社，到大一醫資系 Java 修課與「網站安全設定分析工具」專題的成長軌跡。
4. **專案作品集展示**：以響應式卡片與原生延遲載入 `<video>` 播放器，展示《匿名投稿入口》、《拾頁》（Threads 私人書架）與《ZC》（雙向任務互動 App）三件獨立製作作品。
5. **互動與無障礙細節**：支援錨點平滑捲動、CSS `scroll-target-group` 與 `IntersectionObserver` 導覽高亮、卡片懸停微浮起過場，並完整支援 `prefers-reduced-motion` 減速偏好。

---

## 🧪 A/B 版本實驗說明（Skills 技能展示區）

本次作業針對「技能展示區（`#skills`）」分別於兩個功能分支實作並建立 Pull Request 進行比較：

| 比較項目 | 版本 A：`feature/skills-bars`（進度條版） | 版本 B：`feature/skills-tags`（圖示標籤雲版 — ✅ 最終採用） |
| :--- | :--- | :--- |
| **呈現形式** | 雙欄水平進度條 ＋ 熟練度百分比數值 | 精簡文字膠囊標籤 ＋ 軟體／項目專屬 SVG 圖示 ＋ 分類篩選器 |
| **優點** | 能呈現各項技能相對投入程度 | 視覺輕巧緊湊、一眼掃描完整工具棧，並可依領域點擊過濾 |
| **合併狀態** | **未採用**（PR 保留供版本對照） | **已合併至 `main`** |

### 採用與未採用原因

- **採用版本 B（`feature/skills-tags` 圖示標籤雲版）的原因**：我的技能涵蓋 16 個跨領域項目（包含 HTML5、CSS3、Python、Java、Git/GitHub、Supabase、Cloudflare、Vercel、Tampermonkey、Telegram Bot、Obsidian、Prompt Engineering、Canva、CapCut 以及羽球、游泳）。使用「精簡標籤＋專屬圖示」不僅大幅提升辨識度與閱讀效率，搭配「程式開發／雲端與版控／自動化與筆記／創作與運動」分類篩選器，更符合我 *Keep it simple, keep it real.* 的簡潔定位。
- **未採用版本 A（`feature/skills-bars` 進度條版）的原因**：當技能數量達 16 項且包含雲端平台、筆記軟體與運動習慣時，逐一標示主觀百分比（如「羽球 85%」、「Obsidian 88%」）缺乏客觀衡量基準，且連續 16 條水平進度條會讓畫面顯得冗長單調，因此決定保留該 PR 作為對照紀錄而不合併至 `main`。

---

## 🔄 版本回復（`git revert`）說明

> 我在這次作業中使用 `git revert`（commit `3a3b65a`）回復了 commit `4073ccb`（`style: experiment with dark inverted sidebar in masthead`），原因是當時嘗試將左側個人資訊欄改為深色反轉色塊（`#161826`），實際檢視後發現深色側欄在淺色雜誌紙感背景中過於沉重突兀，破壞了整體雙欄排版的留白呼吸感與文字對比一致性；因此透過 `git revert` 安全抵銷該次樣式變更，既恢復清爽版面，也完整保留了設計實驗的歷史紀錄而不抹除提交軌跡。
