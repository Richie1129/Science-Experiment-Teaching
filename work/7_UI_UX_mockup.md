# UI/UX Mockup 設計

## 設計理念與原則

### 核心設計理念
1. **兒童友善**: 適合小學生使用的介面設計
2. **直觀操作**: 最小化學習成本，專注於實驗學習
3. **視覺化回饋**: 清楚的進度指示和狀態顯示
4. **響應式設計**: 支援各種裝置和螢幕大小
5. **認知負荷最小化**: 避免資訊過載，分步驟呈現

### UX 設計原則
- **可用性優先**: 功能易於發現和使用
- **一致性**: 整個系統保持設計一致性
- **即時回饋**: 所有操作都有明確的回饋
- **錯誤預防**: 設計防止錯誤操作
- **可訪問性**: 考慮不同能力的使用者需求

## 學生端介面設計

### 首頁設計 (index.html)
```
┌─────────────────────────────────────────────────┐
│ 🧪 科學實驗小幫手              [我是教師] 按鈕  │
├─────────────────────────────────────────────────┤
│                                                │
│  ┌──────────────┐  ┌─────────────────────────┐  │
│  │ 📋 實驗選擇   │  │ 🧪 實驗步驟區            │  │
│  │             │  │                        │  │
│  │ 我今天想做的   │  │ 📦 實驗材料:            │  │
│  │ 實驗是:       │  │ • 水盆                  │  │
│  │             │  │ • 透明玻璃杯             │  │
│  │ [選擇實驗▼]   │  │ • 衛生紙               │  │
│  │             │  │ • 水                   │  │
│  └──────────────┘  │                        │  │
│                   │ 🔬 實驗步驟:            │  │
│                   │ ☑️ 1. 準備水盆並裝水     │  │
│                   │ ☑️ 2. 將衛生紙塞進杯底   │  │
│                   │ ⬜ 3. 反轉玻璃杯下壓     │  │
│                   │ ⬜ 4. 慢慢拿出杯子       │  │
│                   │                        │  │
│                   │ 💬 我有問題！            │  │
│                   │ [輸入問題...] [提問]    │  │
│                   └─────────────────────────┘  │
└─────────────────────────────────────────────────┘
```

**設計特點**:
- **清楚分區**: 左側選擇，右側操作
- **視覺圖示**: 使用表情符號增加友善感
- **進度視覺化**: 勾選框顯示完成狀態
- **即時互動**: 問答區域醒目顯示

### 實驗進行中的介面狀態
```
┌─────────────────────────────────────────────────┐
│ 🧪 科學實驗小幫手 - 濕與乾的秘密                 │
├─────────────────────────────────────────────────┤
│                                                │
│  進度: ████████░░ 80% 完成                      │
│                                                │
│  🔬 當前步驟 (3/5):                            │
│  ┌─────────────────────────────────────────────┐│
│  │ 反轉玻璃杯，使杯口朝下，然後將杯子緩慢地     ││
│  │ 下壓進水裡。                               ││
│  │                                            ││
│  │ 💡 提示: 注意觀察水位變化                   ││
│  │                                            ││
│  │           [✅ 我完成了這個步驟]               ││
│  └─────────────────────────────────────────────┘│
│                                                │
│  💬 問答記錄:                                  │
│  ┌─────────────────────────────────────────────┐│
│  │ 🙋 我: 為什麼要緩慢下壓？                   ││
│  │ 🤖 AI: 緩慢下壓可以讓你更清楚觀察到空氣被   ││
│  │     壓縮的過程，也可以避免水花飛濺...       ││
│  └─────────────────────────────────────────────┘│
│                                                │
│  [輸入新問題...] [❓ 提問]                      │
└─────────────────────────────────────────────────┘
```

**設計特點**:
- **進度條**: 清楚顯示整體進度
- **當前步驟強調**: 高亮顯示當前操作
- **問答歷史**: 保留學習脈絡
- **大按鈕設計**: 適合觸控操作

## 教師端介面設計

### 教師管理頁面 (teacher.html)
```
┌─────────────────────────────────────────────────┐
│ 🎓 教師管理頁面                    [登出] 按鈕  │
├─────────────────────────────────────────────────┤
│                                                │
│  ┌──────────────┐  ┌─────────────────────────┐  │
│  │ 📊 快速統計   │  │ 🧪 實驗管理              │  │
│  │             │  │                        │  │
│  │ 實驗總數: 4   │  │ [➕ 新增實驗]           │  │
│  │ 學生使用: 156 │  │                        │  │
│  │ 今日提問: 23  │  │ 現有實驗:               │  │
│  │             │  │                        │  │
│  └──────────────┘  │ 📋 濕與乾的秘密 [編輯][刪] │  │
│                   │ 📋 水杯中的乾燥紙團 [編輯][刪]│  │
│                   │ 📋 衛生紙的濕與乾 [編輯][刪] │  │
│                   │ 📋 探究空氣與水的關係 [編輯][刪]│  │
│                   └─────────────────────────┘  │
│                                                │
│  ┌─────────────────────────────────────────────┐│
│  │ 📈 學習數據分析                             ││
│  │                                            ││
│  │ 最受歡迎的實驗: 濕與乾的秘密 (45%)           ││
│  │ 平均完成時間: 12.5分鐘                      ││
│  │ 常見問題: "為什麼紙不會濕？" (23次)          ││
│  │                                            ││
│  │ [📊 詳細報告] [📥 匯出數據]                 ││
│  └─────────────────────────────────────────────┘│
└─────────────────────────────────────────────────┘
```

### 新增/編輯實驗介面
```
┌─────────────────────────────────────────────────┐
│ ✏️ 編輯實驗: 濕與乾的秘密           [儲存] [取消] │
├─────────────────────────────────────────────────┤
│                                                │
│  實驗名稱: [濕與乾的秘密                    ]  │
│                                                │
│  📦 實驗材料:                                  │
│  • 水盆（可用大碗或盆子替代） [刪除]            │
│  • 透明玻璃杯（或塑膠杯） [刪除]                │
│  • 衛生紙（團成球狀） [刪除]                    │
│  • 水 [刪除]                                  │
│  [➕ 新增材料]                                │
│                                                │
│  🔬 實驗步驟:                                  │
│  1. 準備水盆並在里面裝約八九分滿的水。 [編輯][刪] │
│  2. 將衛生紙團捏成一個小球，然後把它塞進... [編輯][刪]│
│  3. 反轉玻璃杯，使杯口朝下，然後將杯子... [編輯][刪]│
│  [➕ 新增步驟]                                │
│                                                │
│  📹 示範影片:                                  │
│  [🎬 目前影片: demo_video.mp4] [🗑️ 刪除]        │
│  [📁 上傳新影片] （支援 MP4, AVI, MOV）        │
│                                                │
│  📝 自動轉錄內容: (影片上傳後自動生成)          │
│  ┌─────────────────────────────────────────────┐│
│  │ 好現在我們準備了一個水盆裡面裝了大概八九分滿 ││
│  │ 的水 然後一個透明的玻璃杯...                ││
│  └─────────────────────────────────────────────┘│
└─────────────────────────────────────────────────┘
```

## 響應式設計 (Mobile/Tablet)

### 手機版學生介面
```
┌─────────────────┐
│🧪 科學實驗小幫手 │
│           [👨‍🏫] │
├─────────────────┤
│                │
│ 我想做的實驗:    │
│ [選擇實驗 ▼]    │
│                │
│ 📦 需要材料:    │
│ • 水盆         │
│ • 玻璃杯       │
│ • 衛生紙       │
│ • 水           │
│                │
│ 🔬 步驟 2/5:    │
│ ┌─────────────┐ │
│ │將衛生紙團捏成│ │
│ │一個小球，然後│ │
│ │把它塞進玻璃杯│ │
│ │的底部。     │ │
│ │             │ │
│ │[✅完成這步驟]│ │
│ └─────────────┘ │
│                │
│ 💬 有問題嗎？   │
│ [輸入問題...]  │
│ [❓提問]       │
└─────────────────┘
```

## 色彩與視覺設計

### 主色調配置
- **主色**: #3498db (友善藍色)
- **輔助色**: #2ecc71 (成功綠色)
- **警告色**: #f39c12 (注意橙色)
- **錯誤色**: #e74c3c (錯誤紅色)
- **背景色**: #ecf0f1 (淺灰色)

### 字體設計
- **主要字體**: 思源黑體 (Noto Sans CJK TC)
- **大小層級**: 
  - 標題: 24px
  - 副標題: 18px
  - 內文: 16px
  - 小字: 14px

### 圖示設計
- **一致風格**: 使用 Remix Icon 圖示庫
- **語義化**: 每個功能都有對應的直觀圖示
- **大小適中**: 確保在各種螢幕上都清楚可見

## 互動設計

### 動畫效果
- **頁面轉換**: 淡入淡出效果 (300ms)
- **按鈕點擊**: 微妙的縮放回饋 (150ms)
- **進度更新**: 平滑的進度條動畫
- **問答顯示**: 由下向上滑入效果

### 狀態回饋
- **載入狀態**: 旋轉載入指示器
- **成功操作**: 綠色勾選動畫
- **錯誤提示**: 紅色邊框閃爍
- **hover 效果**: 輕微的陰影和顏色變化

## 可訪問性考量

### 視覺可訪問性
- **對比度**: 所有文字與背景對比度 ≥ 4.5:1
- **字體大小**: 支援瀏覽器字體縮放
- **色彩**: 不僅依賴色彩傳達資訊

### 操作可訪問性
- **鍵盤導航**: 所有功能都可透過鍵盤操作
- **觸控**: 按鈕大小 ≥ 44px × 44px
- **語音**: 支援螢幕閱讀器

### 認知可訪問性
- **簡潔性**: 避免不必要的複雜性
- **一致性**: 相同功能在不同頁面保持一致
- **錯誤處理**: 清楚的錯誤訊息和修正建議 