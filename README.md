# 思維框架知識庫 ＆ 無雜訊顧問簡報入口網 (Mental Models Hub)

> 系統：David Cloud 2.0 ｜ 專業管理 · 個人成長 · 思維框架  
> 核心理念：以頂尖管理顧問方法論（McKinsey、BCG、Accenture）與認知科學，驅動指數躍遷與決策複利。

---

## 🌟 核心特色

1. **入口網站與模組化知識庫**：
   - 整合所有思維模型條目、作者背景、核心論題與 David 行動池。
   - 支援即時關鍵字搜尋（即打即查）與分類標籤過濾。
2. **無雜訊頂尖顧問簡報（Zero-Noise Presentation）**：
   - 套用森秀明 8 大無雜訊簡報版型與三大顧問視覺系統。
   - 支援線上互動式簡報閱讀（含鍵盤快速鍵、全螢幕與顧問演講講稿抽屜）。
   - 提供 16:9 `.pptx` 實體簡報檔案下載。
3. **高擴充性架構（Extensible Architecture）**：
   - 數據與視圖完全分離，所有思維模型定義於 `data/frameworks.json`。
   - 未來擴充新書籍或模型時，僅需在 JSON 增加配置項，前台即自動渲染新卡片與搜尋索引。

---

## 📂 檔案目錄架構

```text
thinking-frameworks-hub/
├── index.html                    # 知識庫主入口首頁（即時搜尋、分類篩選、深度彈窗）
├── deck-10x.html                 # 《10倍成長思維》線上互動簡報（12頁顧問精華）
├── data/
│   └── frameworks.json           # 知識庫資料集（未來新增書籍/模型直接在此擴充）
├── assets/
│   └── 10倍成長思維_無雜訊顧問簡報.pptx  # 實體 16:9 PowerPoint 簡報檔
└── README.md                     # 本專案說明文件
```

---

## 🚀 未來資料擴充指引 (How to Add New Models)

欲新增一本新書或新思維框架（例如：`#003 萬維鋼現代思維工具 100 講`）：

1. **萃取知識與產出簡報**：
   - 使用 `/zero-noise-pptx` 產出對應的 `deck-xxx.html` 與 `assets/xxx.pptx`。
2. **更新數據層**：
   - 在 `data/frameworks.json` 中新增一筆 JSON 物件：
   ```json
   {
     "id": "new-framework-id",
     "code": "#003",
     "title": "框架名稱",
     "category": "分類名稱",
     "categoryKey": "strategy | cognition | mental-models | leadership",
     "tags": ["標籤1", "標籤2"],
     "author": "作者",
     "date": "2026-XX-XX",
     "status": "已完成",
     "hasSlides": true,
     "slidesUrl": "deck-xxx.html",
     "pptxFile": "assets/xxx.pptx",
     "summary": "一句話核心洞察...",
     "coreThesis": "底層邏輯...",
     "frameworks": [...],
     "actionItems": [...]
   }
   ```
3. **即時生效**：
   - 首頁 `index.html` 將自動載入並建立即時搜尋索引與互動卡片。

---

## 🌐 線上部署 (GitHub Pages)

本專案透過 GitHub Pages 自動部署上線，全域 CDN 加速存取。
