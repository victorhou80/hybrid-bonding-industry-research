# 来源映射与证据边界（公开安全快照）

**适用文件：** `public-research-summary-draft.md`
**规则：** 仅使用 `R-A–R-E / L-C0 / P01–P09 / A1-Ø / A6`。R 类与 L-C0 只能支持脱敏主题级结论；公开版不得回链、上传或检索原始 ASIC 受限材料。

## 证据标签

| 标签 | 可支持 | 不可支持 |
|---|---|---|
| R-A | 3D 架构、HB/TSV/RDL/bump 分层问题；历史工程计划和带宽模型存在。 | 当前产品、实际接口、准确性能、量产、出货、供应商、客户、收入。 |
| R-B | 公开专利涉及的技术主题、历史脉络和待核验权属事项。 | 资产归属、专利池合并、许可、FTO、产品采用、供应关系、销量。 |
| R-C | 3D EDA、PDK、DFT、KGD、热/PDN、测试与 repair 等工程工作包。 | 已签核、回片、流片、认证、许可合同、量产良率。 |
| R-D | 制造/封装/测试需求字段、供应链模块、产能分层和可证伪模型。 | 中标、订单、价格、BOM、MOQ、交期、有效产能、交付。 |
| R-E | 项目时间、主体、单位、规格和术语错配风险。 | 法人同一、资产承继、客户/供应关系、产品归属。 |
| L-C0 | HB/TSV 工程控制主题：密度/几何、对准、TTV、翘曲、表面、缺陷、测试、可靠性。 | 任一精确本地数值、规则、版图、recipe、测试结果、项目或商业关系。 |
| A1-Ø | 当前公开范围内未形成“明确 pitch/overlay + SKU + 客户/验收 + 交付/收入”的 A1 闭环。 | 技术、产能、项目或市场为零。 |
| A6 | 明确公式和假设的几何或商业情景。 | 实际 I/O、有效 WPM、销量、销售额或市场份额。 |

## 公开来源 P01–P09

| ID | 来源 | 可引用的限定事实 | 等级 | 不可外推项 |
|---|---|---|---:|---|
| P01 | [TSMC SoIC](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/SoIC.htm) | bond pitch 从 sub-10 µm rule 起；3 nm chip stacking 于 2025 年进入 volume production；有 CoW/WoW 页面对象。 | A2 | SKU pitch、overlay、yield、WPM、客户或 die 出货。 |
| P02 | [EVG 6200∞ BA](https://www.evgroup.com/products/bonding/bond-alignment-systems/evg6200-infinity-ba) | backside `±2 µm (3σ)`、transparent `±1 µm (3σ)` 是指定工具 alignment 规格。 | A2 | 产品 post-bond overlay、端到端 yield、客户装机/出货。 |
| P03 | [imec/EVG 1.8 µm W2W announcement](https://www.evgroup.com/company/news/detail/imec-and-evg-demonstrate-for-the-first-time-1-8-m-pitch-overlay-accuracy-for-wafer-bonding-1556544424) | hybrid/via-middle 1.8 µm pitch；另一 dielectric/via-last 分支为 300 nm overlay。 | A3 | 跨分支挪用数值、产品良率或发货。 |
| P04 | [Leti/EVG 1 µm direct HB announcement](https://www.evgroup.com/company/news/detail/leti-demonstrates-world-s-first-300-mm-wafer-to-wafer-direct-hybrid-bonding-with-1-micron-pitch-on-ev-group-system-1556468468) | 300 mm W2W Cu/oxide research demo：1 µm pitch、195 nm overall overlay（3σ）、mean <15 nm。 | A3 | 客户量产、产品 yield、商业出货。 |
| P05 | [imec W2W HB toward 400 nm](https://www.imec-int.com/en/articles/wafer-wafer-hybrid-bonding-pushing-boundaries-400nm-interconnect-pitch) | 300 mm Cu/SiCN W2W HB：400 nm pitch、overlay <150 nm；<100 nm 为 HVM 所述控制目标。 | A3 | 将 <100 nm 写成已达成量产 KPI、产品 yield/出货。 |
| P06 | [imec high-density front/backside connectivity](https://www.imec-int.com/en/articles/path-high-density-front-and-backside-wafer-connectivity) | W2W HB toward 250 nm pitch；TDV/nTSV 指定研究对象含 120 nm pitch。 | A3 | TDV/nTSV = HBM TSV/通用 TSV，或任何产品产能。 |
| P07 | [imec/EVG 200 nm HB test vehicle](https://www.evgroup.com/company/news/detail/imec-and-ev-group-demonstrate-wafer-to-wafer-hybrid-bonding-with-200nm-interconnect-pitch-and-record-high-overlay-accuracy) | 300 mm、four-layer routable **test vehicle**：200 nm Cu pad pitch；100% die post-bond overlay vector <40 nm。 | A3 | 客户产品、商品化批量、量化 product yield、实际 shipped die。 |
| P08 | [Besi Datacon 8800 CHAMEO ultra plus AC](https://www.besi.com/products-technology/product-details/product/datacon-8800-chameo-ultra-plus-ac/) | Hybrid Bonding 工具、ISO3、inline IR inspection、demonstration/sample builds。 | A2 | 未披露的精度、吞吐、客户、量产或收入。 |
| P09 | [Besi Hybrid Bonding 产品组](https://www.besi.com/products-technology/productgroup/hybrid-bonding/) | 光学对准、洁净度、高密度互连和高 yield/performance 的平台级描述。 | A2 | 数字化精度、产出、客户或商业化结果。 |

## 使用与复核要求

1. P01–P09 在被加入新的公开报告前，必须通过 Codex 内置浏览器复核网页对象、时间、原文与不可证明项；
2. 每个数字必须注明是工具规格、研究测量、设计 margin、平台状态还是 A1 实际交付；
3. 加入公司、产线、价格、批量、订单、客户或市场份额前，须新建 A1 证据卡，不能复用 R 类、L-C0、A2、A3 或 A6；
4. 专利权属应逐件用 CNIPA 或经授权法律材料复核，不以本文件代替法律意见。
