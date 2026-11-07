# A股五模型动态集成研究框架

- [公开仓库](https://github.com/Dxfory/5machine_learning)
- [方法说明](https://github.com/Dxfory/5machine_learning/blob/main/README.md)

在JoinQuant环境下将滚动训练、模型动态加权、股票评分与调仓串成研究框架。

| 方法模块 | README明确的设计 |
|---|---|
| 5模型 | LightGBM、XGBoost、SVR、Random Forest、Linear Regression |
| 因子输入 | 约79候选因子：基本面、估值、技术、风险 |
| 动态训练窗 | 按波动状态选择24/36/48个月 |
| 训练与组合节奏 | 约60交易日再训练、10交易日调仓、Top5 |
| 集成权重 | 未来收益MSE与三分类准确性项的combined loss，结合最近3轮损失与弱模型惩罚 |
| 降冗余 | 相关图阈值绝对相关性大于0.6，每簇保留代表因子 |

这些是框架参数，不是实际收益、79个有效alpha或性能领先证据。仓库依赖聚宽API；行业中性化、交叉验证等出现在roadmap的部分不当成已完成。该公开作品与华泰/QBX经历的关系须在个人贡献叙述中单独确认，不迁移其他项目的IC/Sharpe到本页。
