# 阿爾卑斯湖光山色 · 21日手冊 (PWA) — 更新版

離線可用、可安裝到主畫面的隨身行程手冊；全部資料內嵌於 index.html。

## 本次更新（依最新行程表）
- 前段維持原手冊結構：Ortisei 7/22–24（3 晚，Luxury B&B August ×2、Residence Magdalena ×1）、維洛納 7/25–27（Casa Marilla ×3 晚）。
- 後段自駕全部改為火車／電車一日遊，並帶入已購票班次時刻：
  - 7/29 因斯布魯克南邊軌道電車（Stubaitalbahn）
  - 7/30 Mittenwald ＋ 洛伊塔施精神峽谷（06:42 出發 / 16:25 返，已購票）
  - 7/31 延巴赫 Jenbach ＋ Achensee 蒸汽齒軌火車（07:33 出發 / 16:51 返，已購票）
  - 8/1 Sankt Jodok am Brenner 南邊山谷鐵道健行
  - 8/2 因斯布魯克自由參觀（Innsbruck Card）
- 返程：8/3 RJ286（10:42 第7月台 / 265車廂 / 座位71,72,73,74,76）已購票；8/4 土耳其航空 MUC 10:40 → IST（14:30/15:50 轉機，很趕）→ TPE 08:05。
- 領隊聯絡：鄧宇翔 +49-15170176267（首頁與資訊頁，可一鍵撥打／複製）。
- 新地點史實均經查證（Achenseebahn 1889 · 歐洲最古老蒸汽齒軌 · 阿亨湖為提洛最大湖 · Jenbach 三軌距車站；Stubaitalbahn 1904；Brenner 鐵路 1867）。

## Service Worker 版本
本版為 alps-v4（內容更新，已強制端點刷新快取）。

## 更新既有 GitHub Pages 部署
你已部署在 repo 的 alps/ 目錄，只需「覆蓋更新」：
1. 用本資料夾的檔案覆蓋 repo 內 alps/ 下的同名檔案（至少 index.html 與 sw.js）。
2. commit 後 push，GitHub Pages 約 1–3 分鐘重新建置。
3. 使用者端下次連線時，Service Worker 偵測到 alps-v3 會自動更新；若手機仍顯示舊版，關閉分頁重開或於瀏覽器清一次快取即可。

## 檔案
index.html · manifest.webmanifest · sw.js（alps-v3）· icon-192/512/512-maskable.png · apple-touch-icon.png
