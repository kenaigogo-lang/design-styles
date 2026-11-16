# 🎨 design-styles 風格型錄

新網頁專案的風格預覽起點。**不 fork 樣式庫**：現成樣式庫都直接從 CDN 引用（版本鎖定），這裡只放：

- `docs/index.html`：型錄首頁，每個樣式一張即時縮圖 → https://kenaigogo-lang.github.io/design-styles/
- `docs/previews/`：每個樣式庫套在同一份範例內容上的完整預覽（daisyUI、Bootswatch 可切換主題）
- `docs/catalog.json`：機器可讀清單（CDN 引用、用法、適合用途），新專案的 Claude 讀這個
- `docs/themes/`：收藏的客製主題（目前：`nba/`，DailyHighlight 採用 C/D/E；`arcade/` 街機排行榜，GameRank 的第二套主題（可與 NES.css 一鍵切換））
- `rules/CLAUDE.md`：個人規則檔，讓每個新的 Claude 對話都知道要先做風格預覽

## 目前收錄

| 樣式 | 來源 | 適合 |
|---|---|---|
| daisyUI 多主題 | saadeghi/daisyui | 一般 App、後台，30 多套配色 |
| Bootswatch | thomaspark/bootswatch | 穩重資訊型網站，25 套 Bootstrap 主題 |
| Pico CSS | picocss/pico | 內容為主、極簡、自動深色模式 |
| NES.css | nostalgic-css/NES.css | 遊戲、趣味、懷舊 |
| 98.css | jdan/98.css | 復古電腦、惡搞小工具 |
| 主題客製 | `docs/themes/` | 需要強烈主題感的專案 |

找更多：[awesome-css-frameworks](https://github.com/troxler/awesome-css-frameworks)、[classless-css](https://github.com/dbohdan/classless-css)

## 規則檔怎麼生效

- **雲端 Claude Code 對話**：雲端環境的啟動腳本會把 `rules/CLAUDE.md` 的內容寫到 `~/.claude/CLAUDE.md`，每個新對話自動讀到。
- **自己電腦上的 Claude Code**：把 `rules/CLAUDE.md` 的內容放到 `~/.claude/CLAUDE.md`（Windows：`%USERPROFILE%\.claude\CLAUDE.md`）。
- 規則要改：改 `rules/CLAUDE.md`，再請 Claude 同步到雲端環境的啟動腳本。

## 新增樣式

1. 在 `docs/previews/` 加一頁，沿用同一份範例內容（卡片、表單、表格）
2. 在 `docs/catalog.json` 加一筆
3. 客製主題放 `docs/themes/<名稱>/`
