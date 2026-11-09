# Kaggle Home Credit — Credit Risk Model Stability｜团队金牌

## 做了什么

这场比赛考的是信用风险模型在时间漂移下能否保持稳定。我负责**时间感知的分组交叉验证**和**手工特征设计**，用消融实验和跨折稳定性检查筛选特征，让模型在时间推移后依然稳健。

公开管线：Polars 对 depth-0/1/2 表做特征聚合，LightGBM + CatBoost 投票推理，再做融合与稳定性后处理。

## 关键数字

| 指标 | 数值 |
|---|---|
| 名次 | **第 9 / 3,856**（前 0.23%），团队 |
| 奖项 | **Competition Gold Medal** |
| 证书日期 | 2024-05-28 |
| 模型 | LightGBM · CatBoost 融合 |

## 链接

- [比赛与排行榜](https://www.kaggle.com/competitions/home-credit-credit-risk-model-stability/leaderboard)
- [公开推理管线 home-credit](https://github.com/Dxfory/home-credit)
- [金牌证书](assets/kaggle-gold-certificate.png)
