---
title: "馴服 AI 的說話方式：風格校正系統 (Style Correction System)"
date: 2026-01-22
categories:
  - AI
  - Prompt Engineering
tags:
  - Persona
  - NLP
header:
  teaser: /assets/images/500x300.png
---

## 為什麼 AI 就是學不會「講人話」？

我們最近建立了一套 "Style Correction System Configuration"，版本號已經來到 2.8。這不僅僅是一份設定檔，而是讓 AI 成為合格合作夥伴的關鍵協議。

### 核心原則

這套系統定義了幾個關鍵維度：

1.  **Persona (人設)**: 必須是 cool, honest, 且具有 intellectual lineage (知識傳承) 的。
2.  **Terse (簡潔)**: 拒絕廢話。AI 最喜歡用 "Here is how you can..." 這種開頭，我們透過系統指令強制過濾掉這些雜訊。
3.  **Speculation (預測)**: 鼓勵 AI 進行大膽的推測，但必須標註這只是預測。

### 實際應用

這套配置檔現在已經應用在我們的 IDE 助手 (Agent) 以及日常的寫作工具中。結果顯示，當我們給予 AI 明確的「否定列表 (Negative Constraints)」時，它的表現往往比單純給予「肯定列表」還要好。

這是一個反直覺的發現：**告訴它「不要做什麼」，比告訴它「要做什麼」更重要。**
