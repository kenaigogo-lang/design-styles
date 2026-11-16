# 街機排行榜（arcade）

CRT 掃描線、霓虹招牌、逐列換色的 HIGH SCORE 榜。來源專案：GameRank（遊戲評分），作為可與 NES.css 一鍵切換的第二套主題。

- `arcade.css`：完整主題，純 CSS、不依賴任何框架。顏色與字體都是 `:root` 上的變數。
- `index.html`：套用範例資料的預覽。

## 用法

```html
<link href="https://fonts.googleapis.com/css2?family=VT323&family=Monoton&family=Noto+Sans+TC:wght@400;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="arcade.css">
<div class="crt"> … </div>
```

主要 class：`crt`（外層，含掃描線）、`marquee`（霓虹標題）、`coin`（主要按鈕）、`stats`（三格統計）、`sel`（分頁）、`chip`（篩選標籤）、`board` + `row` + `c0`–`c5`（排行榜列與逐列換色）、`mback` + `mbox`（對話框）、`seg`（分段按鈕）、`btn` / `btn go`、`link`。

## 注意

- 只有深色，沒有淺色版。
- VT323、Monoton 沒有中文字，中文一律落到 Noto Sans TC，所以中文內容請用 `--tc` 字體的元素（列名稱、評語、表單）。
- 清單式版面，封面縮圖很小；適合「排名、分數」是主角的內容，不適合以圖片為主的內容。
