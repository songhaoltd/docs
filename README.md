# 嵩昊對外文件站

各品牌／各對象的對外資料頁，透過 GitHub Pages 發佈。

## 網址規則

`https://<pages 網域>/<品牌>-<對象>/`

| 路徑 | 對象 | 狀態 |
|---|---|---|
| `plainpod-doctor/` | GCPlus 開箱醫師 | 上線 |
| `plainpod-kol/` | KOL／通路買手 | 待製作 |
| `plainpod-consumer/` | 消費者 | 待製作 |

## 規則
- 一個對象一個資料夾，內含 `index.html`（單檔、圖片一律 base64 內嵌，不依賴外部資源）
- 未上市產品一律加 `<meta name="robots" content="noindex, nofollow">`
- 原始檔與建置腳本住 Drive `10_品牌行銷/07_品牌／產品介紹/<品牌>/_製作原始檔/`，不進本 repo
