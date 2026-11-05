# James Lin 個人作品集網站 | UI/UX 設計師與網站專案經理

> 一個採用嚴格**瑞士國際主義設計風格（Swiss International Typographic Style）**打造的個人響應式作品集網站。具備無縫的日夜模式切換、背景音樂控制器、Google 試算表聯絡表單串接，以及最先進的 AI 搜尋與解答引擎最佳化（AIO / AEO）佈局。

## 📐 設計哲學 (Swiss International Style)

本專案嚴格遵循瑞士國際主義設計風格（International Typographic Style）：

* **12 欄網格系統**：精準對齊與結構化排版，營造強烈的秩序感。
* **高對比極大化字體**：利用視窗比例（`vw`）呈現極大化的出血標題。
* **零擬物設計 (Zero Skeuomorphism)**：無圓角（`border-radius: 0`）、無陰影、無漸層。
* **嚴格的色彩配置**：米白（`#F4F4F0`）、近黑（`#111111`）、淺灰（`#BDBDB8`）與信號紅（`#E30613`）。

## ✨ 核心功能特色

### 1. 視覺與排版
* **出血排版標題**：首頁標題刻意超出畫面邊緣，營造強烈視覺張力。
* **全站響應式設計 (RWD)**：完美適配手機、平板與桌機。
* **平滑滾動 (Smooth Scrolling)**：點擊錨點連結時提供流暢的頁面轉場。

### 2. 互動與多媒體
* **日夜模式切換 (Dark/Light Mode)**：透過頂部 Font Awesome 圖示（太陽/月亮）無縫切換全站色彩。
* **背景音樂播放器**：頂部配置 Font Awesome 喇叭開關，具備非同步載入（Promise）與錯誤防呆處理。
* **動態懸停回饋 (Hover Effects)**：作品與按鈕在游標經過時產生高對比反白。

### 3. 表單與資料串接
* **客製化聯絡表單**：包含姓名、信箱與留言內容。
* **Google Sheets 自動寫入**：前端透過 `fetch` 與 `application/x-www-form-urlencoded` 格式傳送，避開 CORS 跨域限制，資料直達 Google Apps Script (GAS) 後端並寫入試算表。
* **防呆與狀態提示**：按鈕具備 `SENDING...` 反灰保護與完成提示。

### 4. 搜尋引擎與 AI 最佳化 (SEO, AIO & AEO)
* **傳統 SEO 與社群預覽**：內建完整的 Meta Tags 與 Open Graph (OG) 標籤。
* **JSON-LD 結構化資料**：宣告 `@type: "Person"` 與 `@type: "WebSite"`，精準綁定姓名、職稱、學歷與核心技能（`knowsAbout`），供 ChatGPT、Gemini 等 AI 搜尋引擎快速抓取（AEO）。
* **無障礙語意標籤**：採用語意化 HTML 標籤並配置 `aria-label`。

## 🛠️ 技術堆疊

* **前端架構**：HTML5, Tailwind CSS (Dark Mode 擴充), Vanilla CSS 自定義變數 (`:root`)。
* **圖示庫**：Font Awesome 6.5.2 (`cdnjs`)。
* **程式邏輯**：原生 JavaScript (ES6+)。
* **後端與資料庫**：Google Apps Script (GAS) + Google Sheets。
* **部署與託管**：GitHub Pages。

## 🚀 快速部署指南

1. **複製儲存庫：**
   ```bash
   git clone https://github.com/jameslin-art/jameslin-art.github.io.git
   ```

2. **設定 Google Apps Script (GAS)：**
   * 將 GAS 指令碼部署為網頁應用程式（執行身分：**我**，誰有權限存取：**任何人**）。
   * 將 `index.html` 中的 `gasUrl` 替換為您的專屬 `/exec` 終端點網址。

3. **部署至 GitHub Pages：**
   * 將程式碼推送至 `main` 或 `gh-pages` 分支，並於 Repository Settings 中啟用 GitHub Pages。

## 📄 授權條款

© 2024 James Lin. All rights reserved. 採用 MIT 授權條款釋出。