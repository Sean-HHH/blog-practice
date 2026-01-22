---
title: "構建多鏈資產儀表板 (On-chain Asset Dashboard)"
date: 2026-01-22
categories:
  - Blockchain
  - Dev
tags:
  - DeFi
  - Ethereum
  - Metamask
header:
  teaser: /assets/images/500x300.png
---

## 為什麼需要一個個人化的鏈上儀表板？

在這個多鏈並行的時代，資產分散在 Ethereum, BSC, Arbitrum, Optimism 等各個角落。使用像是 DeBank 或 Zapper 當然很方便，但身為一個開發者，能夠完全掌控自己的數據，並且針對特定的協議（如 Uniswap V3 的流動性部位或 Aave 的借貸狀況）進行客製化監控，是一種難以言喻的樂趣。

### 技術堆疊

這次的專案我選擇了以下的技術組合：

- **Frontend**: React + Next.js
- **Web3**: ethers.js / wagmi
- **Data Fetching**: The Graph (用於 Uniswap 數據), Alchemy (RPC 節點)

### 核心功能

1.  **錢包整合**: 透過 MetaMask 連接，自動識別當前網路。
2.  **餘額聚合**: 掃描多個 EVM 兼容鏈的原生代幣與 ERC20 代幣餘額。
3.  **協議層分析**: 不只是看餘額，更要深入合約層面，解析 LP Token 的組成。

實作過程中最大的挑戰在於處理不同鏈上的 RPC 速率限制，以及如何正規化來自不同協議的數據格式。

接著我會陸續分享更多關於合約互動的細節代碼。
