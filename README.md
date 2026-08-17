# 嵩昊對外文件站

各品牌對外的**產品事實**頁（HTML），透過 Pages 發佈。

## 層級

```
嵩昊（SONG HAO CO LTD）
└── 品牌 ── 對象
    plain-pod/doctor      醫師
    plain-pod/kol         KOL／通路買手
    plain-pod/consumer    消費者
    chimgu/…              自有寢具品牌
    nubizio/…             代理品牌
```

網址：`https://<網域>/<品牌>/<對象>/`

> **註**：CHIMGU 有雙重身分——既是自有品牌，也是販售 PlainPod／nubizio 的零售通路。
> 本 repo 的 `chimgu/` 只放**品牌自身**的產品事實；通路面的東西（上架圖文、檔期）住 Drive `10_品牌行銷/04_官網與通路資產`。

## 這裡放什麼、不放什麼

| | 載體 | 分版依據 | 放這裡嗎 |
|---|---|---|---|
| **產品事實**（認證、成分、規格、使用方法） | HTML | 對象 | ✅ |
| **報價**（價格、分潤、檔期、獨家條件） | PDF 報價單 | 通路／廠商 | ❌ **絕不放** |

**判準一：構成承諾的內容一律不上網頁。** 報價需要「當天談的就是這個數字」的存證，走 PDF 並進該對象的「報價與議價紀錄」（vault 強制規則 #4）。

**判準二：只收會迭代的 HTML。** 凍結的交付文件（議價紀錄、報價單快照）留在 Drive，不進 git——一份檔案住兩處會製造版本分歧。

## 規則
- 一個對象一個資料夾，內含 `index.html`
- **單檔自足**：圖片一律 base64 內嵌，不依賴外部 CDN／字體／圖床
- 未上市產品加 `<meta name="robots" content="noindex, nofollow">`
- 原始檔與建置腳本住 Drive `10_品牌行銷/07_品牌／產品介紹/<品牌>/02_產品介紹/_製作原始檔/`，**不進本 repo**

## ⚠️ Pages 沒有隱私
即使 repo 設為 private，**發佈出去的網站仍然是公開的**（私有 Pages 只有 GitHub Enterprise Cloud 才有）。
`noindex` 與 `robots.txt` 只擋守規矩的爬蟲；**public repo 的原始碼本身就能被搜到**。需要存取控制的內容不要放這裡，走 `songhaoltd/internal`（private）＋ Cloudflare Access。

## 待辦
- [ ] 綁自訂網域 **`docs.songhaoltd.com`**（公司主網域；`chimgu.com.tw` 是消費者品牌官網，不混用）
- [ ] 建 `songhaoltd/internal`（private）收內部工具頁，之後由 `hub.songhaoltd.com` 提供
- [ ] 累積三個以上對外連結後，建「對外連結清單」＋死鏈偵測（接進每日待辦摘要）
