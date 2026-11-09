# QBX｜跨市场因子与策略研究体系

## 做了什么

面向持牌私募的研究需求，搭建覆盖 **美股 · 港股 · A 股 × L1 / L2 / L3** 数据层级的因子与策略研究体系。美股与 A 股、L1/L2 数据上，有数百条平台认证策略。

研究回测的口径：1,700+ backtests run through the research pipeline across the QBX platform and an in-house strategy factory。结构化策略 IR 的口径：690+ structured strategy IRs from the same research pipeline。

- **假设 → 表达式**：把策略假设写成可检验的因子与策略表达式
- **数据与因子筛选**：日频与 L2/L3 微观结构数据，按交易成本、相关性和样本外表现分层筛选
- **门控验证**：分阶段研究集与确认集，Deflated Sharpe ≥ 0.95 门控
- **引擎对齐**：本地解释器与平台成交、指标口径逐项对齐
- **独立复现**：第二套实现独立重算，交叉核验信号
- **参数扫描**：批量 sweep 实验定位稳定参数区间

## 关键数字

| 指标 | 数值 |
|---|---|
| 平台数据集 | **22** |
| 平台策略 | **3,101** |
| Sweep 实验 | **129** |
| A 股 L2 训练结果 | **1,072**，最佳 Sharpe **1.29** |
| 平台认证策略 | Hundreds of platform-certified strategies across US and A-share markets, on L1/L2 data |
| 研究管线回测 | **1,700+** backtests run through the research pipeline across the QBX platform and an in-house strategy factory |
| 结构化策略 IR | **690+** structured strategy IRs from the same research pipeline |
| 引擎对齐 Sharpe | 本地 **1.0814** vs 平台 **1.0820** |
| 独立复现 IC 相关 | **0.998** |
| Deflated Sharpe 门控 | **≥ 0.95** |

## 链接

- 平台：[qbxwin.com](https://qbxwin.com)
- 主页概览：[Dxfory](https://github.com/Dxfory)
