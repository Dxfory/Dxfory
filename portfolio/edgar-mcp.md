# EDGAR Filings MCP｜让 AI 智能体引用 SEC 原始披露

## 做了什么

独立设计、实现并发布了一个 MCP 服务：Cursor、Claude 等智能体可以直接调用 SEC 披露数据，并且每个数字都附带 accession、期间、XBRL 概念和 EDGAR 链接，可以逐条回查原始文件。

4 个工具：
1. `get_trading_symbols`：10-K / 10-Q 中的全部交易代码
2. `get_segment_revenue`：产品、业务、地区维度的 XBRL 分部收入
3. `get_bdc_nonaccrual`：BDC 非应计比例、公允价值、具体投资与抽取方法
4. `get_form4`：Form 4 交易明细，按公开市场交易、授予、行权、代扣税分类

工程上：stdio MCP 服务，离线测试 + CI，推送 tag 后通过 PyPI Trusted Publishing 自动发布到 PyPI、GitHub Release 和 MCP Registry。

## 关键数字

| 指标 | 数值 |
|---|---|
| 当前版本 | **v1.1.3**（2026-11-09 发布） |
| 发布渠道 | PyPI · GitHub Release · MCP Registry（`io.github.Dxfory/edgar-mcp`） |
| 工具 | **4** |
| 离线测试 | **21** 项，CI 通过 |
| 许可证 | MIT |

## 链接

- [GitHub 仓库](https://github.com/Dxfory/edgar-mcp)
- [PyPI：edgar-filings-mcp 1.1.3](https://pypi.org/project/edgar-filings-mcp/1.1.3/)
- [Release v1.1.3](https://github.com/Dxfory/edgar-mcp/releases/tag/v1.1.3)
- [MCP Registry](https://registry.modelcontextprotocol.io/v0.1/servers?search=io.github.Dxfory/edgar-mcp)
