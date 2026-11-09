# 稳定币时序网络 Motif 研究

## 做了什么

用时序网络 motif 研究以太坊上稳定币的转账结构，覆盖 2022 年 5 月 UST/LUNA 崩盘窗口：

- **数据**：通过 Etherscan API 抓取 ERC-20 转账，清洗后按资产拆分
- **时序图**：用 Raphtory 构建转账时序图
- **三节点时序 motif**：1 小时与 1 日两种尺度，输出 motif 热图
- **随机零模型**：打乱时间戳构造对照图，突出真实结构
- **中心性与角色**：Degree、PageRank、Betweenness，再按阈值分为 Seller / Buyer / Shop
- **异常检测**：DBSCAN、Isolation Forest 与分位阈值
- **跨资产关联**：崩盘前后各稳定币日交易额的 ±7 日滞后互相关

仓库根目录保留两张主图：`USDT_1h_motifs_heatmap.png` 与 `motif_heatmap_null_model.png`。USDT、USDC、DAI、UST、LUNA 的 1 小时 / 1 日热图，以及其余图，在 `figures/`。流水线模块是根目录的 `.py` 文件。探索笔记本在 `notebooks/`，未命名草稿在 `notebooks/archive/`。

## 关键数字

| 指标 | 数值 |
|---|---|
| 资产 | **5**：USDT · USDC · DAI · UST · LUNA |
| Motif 尺度 | 1 小时 · 1 日 |
| 方法 | 时序 motif · 随机零模型 · 中心性 · 异常检测 · 互相关 |
| 主图 | `USDT_1h_motifs_heatmap.png` · `motif_heatmap_null_model.png` |

## 链接

- [研究代码、notebook 与图形资产](https://github.com/Dxfory/Understanding-cryptocurrency-transactions-with-network-motifs)
