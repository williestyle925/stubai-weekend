# Stubai × Dresdner Hütte — 山屋週末 PWA

離線可安裝的週末行程手冊。2026/07/11–12,Innsbruck 出發,2 人。
上坡用走、下坡搭纜車;週六登頂 TOP OF TYROL,週日走 Egesensee → Mutterberger See 環線。

## 檔案
- `index.html` — 單頁應用(內含所有 CSS/JS;Day1/Day2 時間軸、海拔剖面、環線圖、票務、費用、山屋資訊、行前清單、第一哩導航、PDF 下載)
- `manifest.webmanifest` — PWA 設定
- `sw.js` — Service Worker(app-shell 離線快取,相對路徑,支援子目錄;目前版本 `stubai-v3`)
- `stubai-handbook.pdf` — A4 列印版手冊(7 頁,對外版,不含住家)
- `icon-192.png` / `icon-512.png` / `icon-maskable-512.png` / `apple-touch-icon.png` / `favicon-64.png`
- `.nojekyll` — 關閉 GitHub Jekyll 處理

## 部署到 GitHub Pages
把本資料夾內**所有檔案放到 repo 根目錄**(不要再包一層)。

命令列:
```bash
cd stubai-pwa
git init && git add -A && git commit -m "stubai weekend pwa"
git branch -M main
git remote add origin https://github.com/<你>/stubai-weekend.git
git push -u origin main
```
或網頁:repo → Add file → Upload files → 拖入所有檔案 → Commit。

接著:repo → **Settings → Pages** → Source 選 `main` / `/(root)` → Save。
約 1 分鐘後開 `https://<你>.github.io/stubai-weekend/`,手機瀏覽器「加入主畫面 / 安裝」。首次連線後即可離線使用。

## 更新內容
改 `index.html` 後,把 `sw.js` 裡的 `stubai-v3` 改成 `stubai-v4`(遞增)以觸發快取更新;push 後重開 App 幾秒即換新版。

字型自 Google Fonts 載入並由 SW 快取;離線時退回系統中文字型。行前清單勾選狀態與第一哩導航偏好存在裝置本機。
