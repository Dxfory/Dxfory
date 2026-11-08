# Agenthon 2026｜ABIDES兼容市场仿真

**Team abc123 · Track 3 Final 第3/55。**

- [赛事官网及Final榜](https://www.agenthon.net/)
- [修订版团队海报](assets/agenthon-2026-t3-poster.pdf)（本仓库内的 1 页 A1 PDF）
- 海报署名：**Peidong Liu · Yiping Yin · Xing Zheng · Team abc123**。这是团队成果，不是 Xing Zheng 的个人独立成绩。
- 海报二维码指向的公开仓库：[EscapedShark/agenthon2026-t3-neurips](https://github.com/EscapedShark/agenthon2026-t3-neurips)
- 官网 Final 榜 T3 分数：**3,249,452.2547**。官网 T2 第8/87、T4 第26/63 是同一团队的跨赛道结果，不是额外奖项。海报没有列出 T2、T4；这两条仍以官网为准，不因海报未写而删除。

## 技术证据

团队以 Rust 重写 ABIDES 兼容市场模拟器（fastsim），并把逐行一致性与性能比较分开。下表来自修订版海报，不是赛事对个人的逐项认证。

| 证据 | 修订版海报口径 |
|---|---|
| Final 展示吞吐 | 约 3.25M rows/s，是吞吐计分。海报写比第 2 名约落后 0.004%。这不是官网分数 3,249,452.2547 |
| 同机速度 | 中位数 880×。比较对象是 ABIDES simulation loop only 与 fastsim whole process。机器与程序：Final binary，i7-10700K，Linux；65 个场景，约 66–1,765×。不是官方容器端到端提速，也不是总分提升 880 倍 |
| 一致性场景 | 2,969 = 95 + 2,274 + 600，发布时 0 row mismatches |
| 容器验证 | 142/142，gates g0–g3 |
| Rust 测试 | 45 tests |
| 镜像 | release 1.26 是版本标签，不是体积。整镜像 1.8 MB：one static binary, empty root |

880× 只是上表规定的同机中位数。海报图里另有一个点标为 ×1,741，落在 66–1,765× 的区间内，不是中位数。海报同时写，这次比较里 ABIDES 的用时是其官方参考时间的 0.96×。

98% 只指 median public unit：72,036 rows，floor 170 ms，占该窗口的 98%。不把它写成所有场景。最大公开单元在海报中另写为该窗口的 78%。

官网总名次仍是 T3 第3/55。2026-11-07 的官网页面把总队数标为 55，其中 54 支有分、1 支标注未计分；这是官网榜的呈现。海报标题写 3rd of 55 teams，结果图写 54 scored teams。海报没有说明第 55 队的状态，本页不推断原因。

## 贡献定位

署名为 Peidong Liu、Yiping Yin、Xing Zheng，队伍 abc123。Xing Zheng 是三人之一。海报成绩按团队使用，不写成个人独立完成，也不代替正式成员记录。

修订版海报原件：[assets/agenthon-2026-t3-poster.pdf](assets/agenthon-2026-t3-poster.pdf)。文件 SHA256：`cfe3efe64669e1237ec24963b51ccef835d0a9bad08f850329e71bd5eeec1a2e`。
