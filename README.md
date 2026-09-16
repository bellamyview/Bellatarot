# 貝拉神秘魔法屋 · 塔羅牌網站

純靜態網站（HTML + CSS + JS，無需任何建置流程），共 80 個檔案：

- `index.html` — 網站主程式（結構、樣式、互動邏輯都在這一份檔案裡）
- `data.json` — 78 張牌的名稱、正逆位關鍵字、牌義說明、愛情/事業/財運/健康解讀
- `images/` — 78 張塔羅牌圖片（依 `data.json` 的 `image` 欄位命名）

## 上傳到 GitHub（網頁上傳）

1. 到 GitHub 建立一個新的 repository（例如 `bella-tarot`）。
2. 進入該 repo，點選「Add file → Upload files」。
3. 把這個資料夾裡的 **所有檔案與 `images` 資料夾** 一起拖曳上傳（共 80 個檔案，未超過 GitHub 網頁單次上傳的 100 個檔案限制）。
4. 送出 commit。

## 部署到 Vercel

1. 到 [vercel.com](https://vercel.com) 用 GitHub 帳號登入。
2. 「Add New → Project」，選擇剛剛的 repo。
3. Framework Preset 選 **Other**（不需要 Build Command，Output Directory 留空或填 `.` 即可，因為這是純靜態網站）。
4. 點 Deploy，等待完成即可拿到網址。

之後如果要更新牌義文字，只要編輯 `data.json`；要換圖片，只要替換 `images/` 裡對應檔名的圖片，重新 commit 到 GitHub，Vercel 會自動重新部署。

## 關於 Firebase

目前這個版本是純靜態網站，**沒有使用到 Firebase**，所以不會有任何費用問題。
如果未來想加入「會員登入」「收藏牌卡」「使用者的解牌紀錄」等功能，才需要接 Firebase（Authentication + Firestore 的免費 Spark 方案即可），到時候可以再另外串接，不會影響現在的網站運作。
