# 工程施工查核委員紀錄系統 PWA

工程施工查核委員紀錄系統 — 支援建築工程、道路排水、廠房工程查核，可安裝為 PWA 在手機或桌面離線使用。

## 快速部署到 GitHub Pages

### 步驟一：建立 GitHub 儲存庫

1. 登入 [GitHub](https://github.com)
2. 點擊右上角「+」→「New repository」
3. 輸入儲存庫名稱（例如：`inspection-app`）
4. 選擇 **Public**（GitHub Pages 免費版需要公開）
5. 點擊「Create repository」

### 步驟二：上傳檔案

將此 ZIP 解壓縮後，把所有檔案上傳到儲存庫根目錄（包含隱藏的 `.github` 資料夾）。

**使用 Git 指令：**
```bash
git init
git add .
git commit -m "Initial commit: PWA inspection app"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/inspection-app.git
git push -u origin main
```

### 步驟三：啟用 GitHub Pages

1. 進入儲存庫 → **Settings** → **Pages**
2. Source 選擇：**GitHub Actions**
3. 儲存設定

### 步驟四：等待自動部署

推送到 `main` 分支後，GitHub Actions 會自動執行部署。
約 1-3 分鐘後，即可在以下網址存取：

```
https://YOUR_USERNAME.github.io/inspection-app/
```

## 安裝 PWA

部署完成後，用手機或電腦瀏覽器開啟網址：

- **Android / Chrome**：點選「加到主畫面」
- **iOS / Safari**：點選分享圖示 → 「加入主畫面」
- **桌面 Chrome/Edge**：網址列右側會出現安裝圖示

## 檔案結構

```
/
├── index.html          # 主應用程式
├── manifest.json       # PWA 設定檔
├── sw.js               # Service Worker（離線支援）
├── icon.png            # 主圖標（原始 2048x2048）
├── icon-72x72.png
├── icon-96x96.png
├── icon-128x128.png
├── icon-144x144.png
├── icon-152x152.png
├── icon-192x192.png
├── icon-384x384.png
└── icon-512x512.png    # 各尺寸圖標（均在根目錄）
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Actions 自動部署
```

## 功能說明

- 工程查核委員現場紀錄
- 支援建築工程、道路排水、廠房工程查核基準
- 缺失紀錄與扣點計算
- 查核評分（Q/W/P）與等級判定
- 列印/預覽查核報告
- 離線使用（Service Worker 快取）
