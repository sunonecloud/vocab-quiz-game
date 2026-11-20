# 主題單字看圖推理小遊戲

針對英文閱讀讀本（每本約 6～10 個主題單字與延伸詞彙）設計的互動看圖答題小遊戲，搭配計分、通關畫面與可透過 **GitHub Pages** 免費發布的網頁架構。

## 核心需求與功能

* **圖文選項與計分通關**：答題時顯示圖片與單字卡片，支援計分、關卡進度顯示與通關結算。
* **點擊才顯示中文提示**：提示預設隱藏，讓學生先自行回憶；有需要時點擊按鈕才會展開中文提示，換題後自動收合。
* **功能／特徵／比較推理問句**：支援詢問住家功能、移動方式、樓層數、周邊環境（如鄰居、魚、樹）或相同／不同特徵，並支援單選與多選（`multi: true`）。
* **易於替換主題與圖片**：將卡片資料（`cardsLibrary`）與題庫（`questionBank`）集中管理，圖片可放於 `images/` 資料夾或使用網址。

## 更新與擴充方式

1. **新增／更換圖片**：將新主題圖片放入 `images/` 資料夾（例如 `images/house.jpg`），並在 `cardsLibrary` 設定 `key`、`word` 與 `img`。
2. **新增／修改題目**：在 `questionBank` 新增題目物件，設定 `question`（英文問句）、`hint`（中文提示）、`answerKeys`（對應卡片的 `key` 陣列）與 `multi`（`false` 單選 / `true` 多選）。
3. **切換不同讀本主題**：
   * **單一更新**：直接修改 `index.html` 內的 `cardsLibrary` 與 `questionBank`。
   * **多主題並存**：為不同讀本建立獨立資料夾（如 `theme1-housing/`、`theme2-animals/`），各自放入 `index.html` 與 `images/`。
4. **發布上線（GitHub Pages）**：將 `index.html` 上傳至 Public Repository，於 **Settings → Pages** 選擇 `main` 分支與 `/ (root)` 儲存即可產生線上遊玩網址；後續直接編輯檔案並 Commit 即可更新。
