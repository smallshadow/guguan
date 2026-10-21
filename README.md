# 谷關工房 · 1020 網頁模型

將此資料夾內的檔案完整上傳到 GitHub 儲存庫，即可部署為靜態網站。不需要安裝套件或執行建置。

## GitHub Pages 上線

1. 建立 GitHub 儲存庫。
2. 上傳本資料夾的**內容**，讓 `index.html` 位於儲存庫根目錄；`assets` 與 `vendor` 也一起上傳。
3. 儲存庫 **Settings → Pages → Build and deployment**，Source 選 **Deploy from a branch**。
4. Branch 選 **main**、資料夾選 **/(root)**，按 Save。
5. 等部署完成，使用 Pages 顯示的網址開啟。

參考：[GitHub 官方 Pages 設定說明](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。如果上傳時保留外層 `guguan-1020-web` 資料夾，網址也須加上 `/guguan-1020-web/`。

## 操作

- 左側按鈕依原 SketchUp 檔案的 22 個場景名稱與順序排列，切換視角及物件顯示狀態。
- 「半透明模型」將目前場景可見的模型表面改為半透明；原場景隱藏的物件仍維持隱藏。
- 「重設視角」回到目前場景的原始角度。
- 滑鼠左鍵拖曳旋轉、滾輪縮放、右鍵拖曳平移。
- 手機單指旋轉、雙指縮放與平移，場景按鈕位於底部。
- 取景範圍會配合螢幕比例調整；標註過密時自動避開重疊，放大後可看到更多文字。

## 本機預覽

請使用 HTTP 服務，不能直接雙擊 `index.html`。電腦已安裝 Python 時，在本資料夾執行：

```sh
python -m http.server 8000
```

再開啟 `http://localhost:8000`。也可使用 VS Code Live Server。

## 來源及內容

- 來源：`谷關工房_天花燈具_含家具1020.skp`，2026-10-21 轉出。
- 原始 SKP 未修改，網站使用轉出的網格、材質、場景與尺寸標註資料。
- 場景 01–22 完整保留；網頁光照、線寬、文字排版與透明疊合效果可能與 SketchUp 略有不同。
- 尺寸標註為原模型資料的網頁顯示，不是新增丈量工具。
- `assets/viewer.json`：場景、材質、尺寸文字與顯示設定。
- `assets/viewer.bin`：網格及線條資料；其餘 PNG 為模型貼圖。
- `vendor`：本機附帶 Three.js 0.170.0 與 OrbitControls，授權見 `vendor/LICENSE-three.txt`。
- 所有資源使用相對路徑，沒有外部 CDN、帳號或 API 金鑰需求。

模型本身的權利歸原權利人；Three.js 授權僅適用於其程式庫。
