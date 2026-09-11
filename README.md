# design-studio-process 範例網站

**線上展示：https://design-studio-process-examples.vercel.app**

用 Agent Skill [design-studio-process](https://github.com/allen-hsu/design-studio-process) 做出來的五個範例網站，加上一個列出它們的展示首頁。每個範例都是單一 HTML 檔，字型已內嵌，沒有建置步驟。

## 範例

| # | 題目 | 測試重點 | 線上 |
|---|---|---|---|
| 1 | 生產力 App landing page | seed 字串、critic 迴圈 | [開啟](https://design-studio-process-examples.vercel.app/examples/01-kite) |
| 2 | 大稻埕茶行一頁式網站 | WebGL 即時 3D、捲動驅動轉場 | [開啟](https://design-studio-process-examples.vercel.app/examples/02-tea-shop) |
| 3 | 記帳 App「今日支出」 | 刪減與「不刪個性」護欄、手勢互動 | [開啟](https://design-studio-process-examples.vercel.app/examples/03-receipt) |
| 4 | 獨立樂團巡演網站 | 大膽提示詞流程、CSS 3D 摺頁 | [開啟](https://design-studio-process-examples.vercel.app/examples/04-night-bus) |
| 5 | 既有 SaaS 官網改版 | 內容盤點、前後客觀檢查 | [改造前](https://design-studio-process-examples.vercel.app/examples/05-shiftflow/before)・[改造後](https://design-studio-process-examples.vercel.app/examples/05-shiftflow/after) |

每個範例測了哪些技巧、哪些沒測到，寫在展示首頁的說明卡上；完整評估在 skill repo 的 [`evals/technique-evaluation.md`](https://github.com/allen-hsu/design-studio-process/blob/main/evals/technique-evaluation.md)。

## 目錄

```
index.html        展示首頁
examples/         五個範例（單一 HTML，字型內嵌）
media/thumbs/     首頁縮圖
vercel.json       乾淨網址設定
.vercelignore     排除 handoff/、.env*、mp4
```

## 部署

靜態網站，不需要建置。Vercel 專案設定：Framework Preset 選 **Other**，Build Command 留空，Output Directory 維持根目錄。

本機部署：`npx vercel`（預覽），確認沒問題後 `npx vercel --prod`。

## 修改頁面時

- 中文字型是依頁面實際用字子集化的。改了頁面文字，要用 skill repo 的 `scripts/embed_fonts.py` 重新子集化，否則新加的字會退回系統字型。
- 改完用 skill repo 的 `scripts/lint_design.py` 檢查，可以直接給線上網址。

## 說明

- 範例中的店名、樂團、公司、電話、價格、數據與客戶見證皆為虛構。`examples/05-shiftflow/before.html` 是刻意寫成典型 AI 風格的測試輸入，不是真實公司的網站。
- 範例 2 的 3D 效果尚未在實體裝置上量測效能。

## 授權

程式碼以 MIT 授權釋出，見 [LICENSE](LICENSE)。內嵌字型皆以 SIL Open Font License 釋出：Noto Sans TC、Noto Serif TC、芫荽 Iansui、Barlow、Barlow Condensed、Fragment Mono、IBM Plex Mono、Archivo Narrow。
