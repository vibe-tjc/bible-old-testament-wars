# Bible Old Testament Wars

互動式靜態網站：呈現聖經舊約著名戰爭的流程、重要事件、地點與信仰功課。

## Tech Stack

- Astro
- TypeScript
- Leaflet + OpenStreetMap
- GitHub Pages

## Development

```bash
pnpm install
pnpm dev
```

## Build

```bash
pnpm build
pnpm preview
```

## Deploy

Push to `main` triggers GitHub Pages deployment via `.github/workflows/deploy.yml`.

Production URL after Pages is enabled:

https://vibe-tjc.github.io/bible-old-testament-wars/

> 地圖功能需要網路連線以載入 OpenStreetMap 圖磚。

## Prompt

可以用以下 prompt 產生類似本站的互動式靜態網站：

```text
請幫我建立一個純前端、可部署到 GitHub Pages 的互動式靜態網站，用來呈現聖經舊約著名戰爭的流程與重要事件。

需求：
1. 使用 Astro + TypeScript 架構，資料與 UI 分離，方便後續維護。
2. 不要後端系統，不需要資料庫。
3. 網站語言使用繁體中文。
4. 至少整理以下舊約戰役：
   - 亞伯蘭救羅得：四王與五王之戰（創世記 14章）
   - 紅海邊的拯救：法老追兵覆沒（出埃及記 14章）
   - 耶利哥城倒塌（約書亞記 6章）
   - 艾城失敗與再次得勝（約書亞記 7–8章）
   - 基甸三百勇士勝米甸（士師記 6–7章）
   - 底波拉與巴拉勝西西拉（士師記 4–5章）
   - 大衛擊敗歌利亞（撒母耳記上 17章）
   - 以利沙與火車火馬：亞蘭軍被引入撒馬利亞（列王紀下 6章）
   - 耶路撒冷脫離亞述王西拿基立（列王紀下 18–19章；以賽亞書 36–37章）
5. 每場戰役需要包含：
   - 標題
   - 經文出處
   - 時期
   - 地點
   - 主要人物
   - 簡介
   - 戰爭流程步驟
   - 重要信仰功課
   - 地圖資料與路線示意
6. 加入搜尋功能，可以搜尋戰役、人物、地點、經文。
7. 加入時期篩選，例如先祖時期、出埃及／曠野、征服迦南、士師時期、王國時期。
8. 整合 Leaflet + OpenStreetMap，讓每場戰役顯示互動式地圖、marker 與路線 polyline。
9. 部署目標是 GitHub Pages repo subpath，例如 `/bible-old-testament-wars/`，請設定 Astro `base`。
10. 注意 Leaflet marker icon 在 GitHub Pages subpath 可能 404，請明確 import `marker-icon.png`、`marker-icon-2x.png`、`marker-shadow.png` 並設定 `L.Icon.Default`。
11. 加入 GitHub Actions workflow，push 到 `main` 後自動 build 並 deploy 到 GitHub Pages。
12. README 需要包含開發、build、部署方式與 production URL。

請產生完整專案檔案，並確保 `pnpm test` 可以執行 `astro check && astro build`。
```
