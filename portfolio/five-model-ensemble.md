# A 股五模型动态集成｜滚动训练与动态加权

## 做了什么

在聚宽（JoinQuant）上搭建了一套多模型、动态加权的 A 股选股系统：

- **五模型集成**：LightGBM · XGBoost · SVR · Random Forest · Linear Regression
- **约 79 个候选因子**：基本面、估值、技术、风险四大类
- **自适应训练窗**：按沪深 300 近期波动选择 24 / 36 / 48 个月
- **combined loss 动态加权**：未来收益 MSE + 三分类准确率，取最近 3 轮平均；损失持续偏高的模型降权（penalty 0.5）
- **降冗余**：相关图阈值 |ρ| > 0.6，每簇保留一个代表因子
- **节奏**：约每 60 个交易日再训练（~60 trading days, ≈ quarterly），每 10 个交易日调仓，持有 Top 5

v1.0 → v2.0 的迭代同时提升了 Sharpe 和收益。

## 关键数字

聚宽研究回测，初始资金 **¥100,000**，区间 2024-11-15 → 2025-11-15。

| 版本 | Sharpe | 收益 |
|---|---|---|
| v2.0 | **2.499** | **70.90%** |
| v1.0 | **2.033** | **58.49%** |

## 链接

- [仓库 5machine_learning](https://github.com/Dxfory/5machine_learning)（`v1.0.png` / `v2.0.png` 为回测截图）
- [方法说明 README](https://github.com/Dxfory/5machine_learning/blob/main/README.md)
