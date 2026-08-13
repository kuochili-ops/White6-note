# 𓃥 白六留言本 (White6 Guestbook)

一個基於 Web 技術構建的擬真 3D 互動電子留言本。專為提供沉浸式閱讀體驗而設計，具備皮革精裝書殼、透明書籤頁、柔和 3D 雙向翻頁動畫與繁體中文全字庫支援。

---

## ✨ 核心特色 (Features)

- **📖 擬真雙頁筆記本結構**
  - **精裝皮革外殼**：細緻的立體邊緣與皮革質感背板。
  - **立體書脊與疊紙厚度**：模擬真實實體書本的裝訂質感與邊緣厚度。
  - **自動頁頭日期**：左頁頂部自動動態生成當天西元日期與星期（如 `2026/08/13 星期四`），顏色與頁面橫線完美統一。

- **🔖 獨立透明書籤頁 (Transparent Ribbon Page)**
  - 首頁疊加獨立的透明書籤頁與紅色緞帶。
  - 當翻至下一頁時，實體紙張會 **100% 完全遮蓋透明書籤**，避免透出或擋字。
  - 修正傳統玻璃模糊濾鏡（`backdrop-filter: blur`）導致底層文字打糊的問題，確保文字 100% 銳利清晰。

- **🚀 60fps 原生級順暢 3D 翻頁 (GPU Accelerated Flip)**
  - **雙向 3D 風吹翻頁**：支援「下一頁 ➔」與「⬅ 上一頁」雙向 3D 頁面過渡。
  - **無殘影無閃爍**：優化 JavaScript 翻頁與 DOM 重繪（Reflow）時機，回翻時絕不露底或閃爍舊頁面殘影。
  - **GPU 硬體加速**：採用 CSS `transition` 與 `will-change: transform` 搭配 `requestAnimationFrame`，在行動端與 iOS WebKit 上實現零卡頓的 60fps 流暢動畫。

- **✍️ 繁體中文全字庫支援 (Chinese Typography)**
  - 整合 Google Fonts 繁體全字庫資源（如 **霞鶖文楷 LXGW WenKai TC**、**Yuji Boku 行書風**、**思源宋體**、**思源黑體**）。
  - 解決常見簡體字型引起的缺字/欠字問題，字型呈現完整美觀。

- **⚙️ 即時選單與自適應視覺 (Responsive & Customizer)**
  - 右上角可收合設定選單，支援即時修改留言內容、字體風格與字體大小。
  - 自動防裁切置中縮放，在手機與平板端皆能完美聚焦左頁內容。
  - 支援「切換視角」功能，可隨時旋轉 3D 傾斜角度。

---

## 🛠️ 技術架構 (Tech Stack)

- **前端語言**：HTML5, CSS3, JavaScript (ES6+)
- **3D 渲染**：純 DOM CSS3D Transform, Perspective, CSS Transitions, GPU Acceleration
- **字體資源**：Google Fonts API
- **相容性**：支援 iOS Safari, Android Chrome, Desktop WebKit/Blink 瀏覽器

---

## 🚀 快速開始 (Quick Start)

本項目為純前端單頁應用程式（SPA），無需安裝額外的 Node.js 包或建置工具：

1. **複製專案 (Clone Repository)**：
   ```bash
   git clone [https://github.com/your-username/white6-guestbook.git](https://github.com/your-username/white6-guestbook.git)
   cd white6-guestbook
