---
title: "Quick-Timer 開發筆記：計時器的分段功能 (Split) 實作"
date: 2026-01-22
categories:
  - Coding
  - Frontend
tags:
  - JavaScript
  - React
  - UI/UX
header:
  teaser: /assets/images/500x300.png
---

## 看似簡單的計時器

前幾天我在優化 Quick-Timer 應用程式時，收到了關於加入「分段計時 (Split)」功能的需求。這聽起來很基本，但在實作細節上卻有不少坑。

### 需求分析

目標是讓使用者在計時過程中，按下 "Split" 按鈕時，能夠記錄當下的時間點，最多記錄 10 筆。這需要精準地捕捉 `requestAnimationFrame` 或是 `setInterval` 中的時間狀態。

### 程式碼思考

```javascript
const handleSplit = () => {
  if (splits.length >= 10) return;
  setSplits(prev => [...prev, currentTime]);
};
```

關鍵在於 `currentTime` 的精準度。如果只用 React state 來驅動重繪，可能會因為 render cycle 而產生微小的誤差。因此我們採用了 `useRef` 來保存真實的開始時間戳記，並在每一幀計算差值，確保 Split 的時間絕對準確。

這就是前端開發有趣的地方：**魔鬼總在細節裡**。
