# Hybrid Bonding / TSV 互连密度与精度证据包

**发布包日期：** 2026-08-01（Asia/Shanghai）

**公开来源资料截点：** 2026-07-31
**用途：** 为本仓库既有的 3D IC、Hybrid Bonding、HBM 与供应链研究补充一份可审计的“互连密度—对准精度”资料包。

## 这份包回答什么

本资料包将四类经常被混写的指标分开处理：

1. Hybrid Bonding 的 `bond / pad pitch` 与由 pitch 得到的**名义几何站点密度**；
2. TSV、TDV/nTSV、bump 与 RDL 的不同物理层级和不同密度分母；
3. alignment / overlay、TTV、bow/warpage、flatness、Cu 表面状态、defect / reliability 等不同“精度”口径；
4. 公开平台、设备规格、研究 test vehicle 与实际产品出货之间的证据边界。

最重要的结论是：**公开资料中的最小 pitch、设备对准规格或测试车 overlay，不能自动推导为产品实际 I/O 密度、良率、有效产能、客户采用或实际出货。**

## 目录内容

```text
README.md                         本说明与使用边界
public-evidence-report.md         公开一手来源支持的指标矩阵与结论
public-source-ledger.md           9 条可复核公开来源、锚点和使用限制
evidence-gaps.md                  13 项尚未由公开证据闭环的问题
local-materials-safe-summary.md   本地受限资料的脱敏主题级审计摘要
publication-manifest.md           本次发布范围与明确排除项
```

## 证据等级

| 等级 | 本包中的含义 | 可用于什么 | 不能用于什么 |
|---|---|---|---|
| **A1** | 法定/审计披露，或制造商与客户共同确认的产品发货、收入、验收、批量交付 | 实际商业交付或收入，且必须保留 SKU、口径和期间 | 未披露的工艺参数、供应商映射或良率 |
| **A2** | 制造商官方平台、工具产品页或官方新闻稿 | 平台状态、公司声明的量产状态、工具规格 | 客户采用、产品级参数、实际 die/wafer 出货 |
| **A3** | 研究机构/设备商公开的联合研究、会议论文、test vehicle 或演示 | 指定结构、指定统计条件下的 pitch、overlay 或测试结果 | 商业量产、跨客户可复制 yield、实际销售 |
| **A6** | 由公开 pitch 做出的透明几何换算 | 名义格点密度与数量级关系 | 实际可用 I/O、可路由率、良品互连数、产能或销量 |
| **C0** | 本地受限工程、规则、检查表或内部测试资料 | 仅能说明相应主题存在并需要被工程控制 | 任何公开数值、产品规格、量产能力、良率或供应链结论 |

## 可直接复核的核心发现

- TSMC 的公开 SoIC 页面属于 **A2 平台证据**：页面称 bond pitch 从 `sub-10 µm rule` 开始，且 3 nm chip stacking 在 2025 年进入 volume production；但没有公开某 SKU 的实际 pitch、overlay、有效 WPM、良率、客户或出货量。
- imec/EVG 的公开 **A3 test vehicle** 证据：2026 年的 300 mm W2W test vehicle 报告 200 nm Cu interconnect-pad pitch，以及全片、100% die 的 post-bond pad-to-pad overlay vector `<40 nm`；这不是客户产品或 A1 实际出货。
- TSV 相关的 120 nm pitch、20 nm bottom-diameter 公开记录对应的是 imec 的 TDV/nTSV 背面细连接研究，不能替代传统 TSV、HBM TSV 或所有 3D IC TSV 的量产规格。
- 在本包覆盖的“带明确 pitch/overlay 数字”的公开一手来源中，能够满足 **A1 实际出货/收入/客户联合验收** 定义的来源数量为 **0**。因此本包不提供“某一纳米 pitch 的实际全球出货量”这一类虚假精确度结论。

## 如何使用

1. 需要数值时，先在 `public-source-ledger.md` 按来源编号复核网页标题、锚点、日期和测量对象；
2. 再从 `public-evidence-report.md` 读取对应的“能证明 / 不能证明”边界；
3. 只有在来源、对象、统计口径、商业状态和可靠性五项都闭环时，才可把技术指标纳入产能、销量或市场模型；
4. 任何与本地资料有关的表述只能使用 `local-materials-safe-summary.md` 中的主题级结论，不能尝试还原或要求上传原始资料。

## 本次发布的安全边界

本目录没有包含、也没有从中推导或转录任何非公开设计、制造、测试、商业关系或访问控制信息。仅保留公开网页可复核的技术事实，以及不含数值和来源定位的本地资料主题级审计结论。

资料仅供产业研究和信息审计，不构成投资、采购、工艺认证或法律意见。
