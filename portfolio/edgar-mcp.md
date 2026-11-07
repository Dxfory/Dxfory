# EDGAR Filings MCP｜已发布金融数据工具

将SEC披露转为可调用、可回查原始来源的金融数据接口。

- [GitHub项目与README](https://github.com/Dxfory/edgar-mcp)
- [正式release v1.1.2](https://github.com/Dxfory/edgar-mcp/releases/tag/v1.1.2)
- [PyPI安装包](https://pypi.org/project/edgar-filings-mcp/)

v1.1.2正式release发布于2026-09-21 18:03:46（北京时间）。

## 4项工具

1. 定期报告交易代码。
2. 产品、业务或地区维度的XBRL分部收入。
3. BDC非应计贷款/资产数据与抽取方法。
4. Form4交易明细，区分公开市场交易、授予、行权及代扣税等类型。

每项金融数据尽可能返回accession、期间、概念与EDGAR链接，使模型回答可以追溯到披露本身。BDC非应计数据不等同于违约率，抽取缺失不直接解释为零风险。

MIT许可，底层使用edgartools。本作品是金融任务接口与数据口径工程，不宣称从零搭建SEC数据库；未以下载次数推导真实用户数。
