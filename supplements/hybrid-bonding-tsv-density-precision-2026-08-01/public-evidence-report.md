# 公开证据报告：Hybrid Bonding / TSV 的互连密度与对准精度

**公开来源资料截点：** 2026-07-31

**适用范围：** 3D IC 的 wafer-to-wafer（W2W）Hybrid Bonding、TSV/背面细互连，以及相关对准工具。
**不适用范围：** 本报告不把设备规格、研究 test vehicle、量产平台状态、专利或市场新闻写成实际产品出货。

## 结论先行

1. **量产平台与最细研究纪录不是同一件事。** TSMC SoIC 的公开表述支持“3 nm chip stacking 于 2025 年进入 volume production”的平台状态（A2）；imec/EVG 的 200 nm pad pitch 与 `<40 nm` post-bond overlay 是 300 mm test vehicle 结果（A3）。两者均不能直接转换为某 SKU 的出货量或良率。
2. **密度必须先说明分子、分母和网格。** 由 pitch 作 `1,000,000 / p_µm²` 的方格换算只得到假设全填充的名义站点密度（A6）；它不等于有效 data I/O、good link、可路由率、Cu fill、产品良率或单位面积销量。
3. **“精度”至少有四种不同对象。** 工具 alignment spec、post-bond overlay、设计/roadmap margin 和量产平台状态不能替代彼此。TTV、bow/warpage、flatness、Cu recess、particle/void 和 reliability 也不能被一个 overlay 数字覆盖。
4. **TSV 必须分层。** 传统 TSV、HBM TSV、2.5D interposer TSV、backside TDV/nTSV、W2W Hybrid-Bond pad，以及 package bump/RDL 的物理对象、工艺约束、价值链和统计口径不同；不应合并为一个“TSV 密度”列。
5. **实际出货仍没有与几何/精度数值闭环。** 本次公开一手来源中，A1（SKU、时间段、交付/收入或客户联合验收）的 “pitch + overlay + actual shipment” 组合证据为 0 项。任何把公开研究数值写为“已规模出货”的说法都不成立。

## 指标矩阵：公开、可复核的事实

| ID | 可复核的公开事实 | 密度/几何信息 | 精度/overlay 信息 | 等级 | 可以写什么 | 不可以写什么 |
|---|---|---|---|---|---|---|
| P01 | TSMC SoIC：bond pitch starts from the `sub-10 µm rule`；3 nm chip stacking entered volume production in 2025 | 仅可做 `>10,000 sites/mm²` 的 A6 尺度参照 | 未公开产品级 overlay | A2 | 平台状态与公开规则尺度 | SKU pitch、良率、客户、WPM、die 出货量 |
| P02 | EVG 6200∞ BA：面向 pilot / volume production 的 W2W bond-alignment tool | 无公开 pitch / I/O 密度 | backside `±2 µm (3σ)`；transparent `±1 µm (3σ)` | A2 | 特定工具的发布规格 | HB 成品 post-bond overlay、客户使用、成品 yield |
| P03 | imec/EVG 2017：hybrid/via-middle W2W 达 1.8 µm pitch；另一 dielectric/via-last 分支的全片 overlay 为 300 nm | 1.8 µm 的 A6 方格参照约 0.309 M/mm² | 300 nm 属于另一 dielectric/via-last 分支 | A3 | 两个研究分支各自的结果 | 将 300 nm 误归给 hybrid 分支，或写成量产良率 |
| P04 | Leti/EVG 2017：300 mm W2W Cu/oxide direct HB，1 µm pitch、最小 500 nm Cu pad | 1 µm 方格参照 1.00 M/mm²；500 nm pad 不等于 500 nm pitch | 195 nm overall overlay（3σ）；mean `<15 nm` | A3 | 生产型系统上的研究演示 | 商业产品量产、客户交付或量化良率 |
| P05 | imec：300 mm Cu/SiCN W2W HB，400 nm pitch、overlay `<150 nm`；研究称 HVM 所需控制应 `<100 nm` | 400 nm 方格参照 6.25 M/mm² | `<150 nm` 为公开结果；`<100 nm` 是 HVM 需求判断 | A3 | 实测与研究门槛的区别 | 将 `<100 nm` 写成已达到的量产 KPI |
| P06 | imec VLSI 2025：W2W HB 向 250 nm pitch 演进；backside TDV/nTSV 为 20 nm bottom diameter、120 nm pitch；有 15 nm layout overlay margin | 250 nm HB 为 16.0 M/mm²；120 nm TDV/nTSV 为 69.4 M/mm²（均 A6） | 15 nm 是设计 margin，不是实测 tool/HB overlay | A3 | 背面细连接的研究边界 | TDV/nTSV 等同所有 TSV 或 HBM TSV |
| P07 | imec/EVG 2026：300 mm、四层可路由 W2W HB test vehicle，200 nm Cu interconnect-pad pitch；全片 100% die post-bond overlay vector `<40 nm` | 200 nm 方格参照 25.0 M/mm²；六角位置参考约 28.9 M/mm² | `<40 nm`，测量对象为全片 test vehicle 的 pad-to-pad overlay vector | A3 | 前沿公开研发/ECTC 测试车精度记录 | 客户产品、商品化批量、A1 shipped die、量化 yield |
| P08 | Besi Datacon 8800 CHAMEO ultra plus AC：ISO3 工作区、inline IR inspection、样品/演示能力 | 无公开量化 pitch | 无公开量化 placement/overlay 值 | A2 | 设备供应链能力说明 | 从 “high accuracy” 虚构具体精度或出货 |
| P09 | Besi Hybrid Bonding 产品组：光学对准、洁净度、高密度互连与性能/yield 的平台描述 | 无量化密度 | 无量化精度 | A2 | 工具平台存在 | 具体吞吐、产品 yield、客户商业化 |

来源链接、读取锚点和逐项限制见 [public-source-ledger.md](./public-source-ledger.md)。

## 名义几何密度：仅限 A6 比较

若公开来源只公布 pitch 而未公布真实可用 I/O 数量，可采用方格全填充的透明基准：

`D_square = (1000 / p_µm)^2 = 1,000,000 / p_µm² sites/mm²`

对于明确公开的六角位置网格，可另给出：

`D_hex = 2,000,000 / (√3 × p_µm²) sites/mm²`

| 公开 pitch | 对象 | 名义方格站点密度（A6） | 审计说明 |
|---:|---|---:|---|
| `<10 µm` | TSMC SoIC platform rule 起点 | `>10,000/mm²` | 未公布确切 p 或实际连接数 |
| `1.8 µm` | imec/EVG 2017 hybrid W2W | `0.309 M/mm²` | 研究结构的几何参考 |
| `1.0 µm` | Leti/EVG 2017 direct HB | `1.00 M/mm²` | 500 nm pad 不可改算成 4 M/mm² |
| `400 nm` | imec Cu/SiCN W2W HB | `6.25 M/mm²` | 研究结果，不是量产 I/O 密度 |
| `250 nm` | imec W2W HB 研究路线 | `16.0 M/mm²` | “high yield”未公布数值 |
| `200 nm` | imec/EVG 2026 W2W test vehicle | `25.0 M/mm²`；六角参考 `28.9 M/mm²` | 25% designed Cu density 不是 active I/O 或 yield |
| `120 nm` | imec TDV/nTSV（非 HB pad） | `69.4 M/mm²` | 不可与 W2W HB 站点相加或混作一个市场分母 |

这张表不是产能、良品数、实际 I/O、可用 die 面积、互连良率或销售额。它没有扣除 Cu fill、dummy pad、keep-out、PDN、RDL、test structure、冗余、故障连接或产品边缘面积。

## 精度口径：不能互换的四类数值

| 数值类别 | 公开例子 | 正确含义 | 禁止外推 |
|---|---|---|---|
| 工具规格 | EVG 的 `±2 µm / ±1 µm (3σ)` | 某工具在声明条件下的 alignment capability | HB 成品 post-bond overlay、客户量产良率 |
| 实验测量 | 195 nm (3σ)、`<150 nm`、`<40 nm vector` | 指定 wafer/test vehicle、工艺流、统计范围下的结果 | HVM Cp/Cpk、跨客户 yield、SKU 性能 |
| 设计 margin / roadmap 需求 | 15 nm layout margin、`<100 nm` HVM 控制要求 | 设计容差或研究的所需目标 | 已测的设备精度或认证量产控制限 |
| 平台量产状态 | “3 nm chip stacking entered volume production” | 平台的官方状态声明 | 产品 pitch、overlay distribution、WPM、销售额 |

另外，flatness/roughness、TTV、bow/warpage、Cu recess/protrusion、particle/void、bond yield、WAT/chain 和可靠性属于不同的制造质量变量。单一 overlay 数值不能替代任一变量。

## Hybrid Bonding、TSV、bump/RDL 的层级关系

| 层级 | 典型作用 | 密度/精度指标 | 常见错误 |
|---|---|---|---|
| W2W/D2W Hybrid Bonding | die/wafer 之间的细间距直接垂直互连 | pad/bond pitch、post-bond overlay、Cu/oxide 表面、void、bond yield | 用封装 bump pitch 代替 HB pitch |
| Traditional TSV | 穿硅导通、可能服务于存储堆叠或中介层等 | diameter、depth、aspect ratio、pitch、keep-out、填充/可靠性 | 用 TSV 数量推导 HB 有效带宽 |
| TDV/nTSV/backside fine interconnect | 背面或介质相关细连接 | bottom diameter、pitch、layout margin、backside lithography | 将研究型 nTSV 当成 HBM TSV 通用规格 |
| micro-bump / C4 / FCBGA | die-to-package、package-to-substrate 或外部 I/O | bump pitch、net density、collapse、warpage、joint reliability | 将外部 100+ µm bump pitch 写成内部 HB pitch |
| RDL | 再布线、fan-out、供电/信号分配 | line/space、via、routing density、IR-drop | 认为 RDL 线宽天然等于垂直互连密度 |

## 对商业与供应链研究的正确含义

技术机会可以讨论，但必须以不同证据层级建模：

1. **A2 平台机会：** 3D PDK/EDA、平坦化与 CMP、清洗、临时键合/减薄、inline overlay/void metrology、热与测试协同；收入仍需产品/客户证据确认。
2. **A3 研发机会：** 200–400 nm W2W HB 相关的对准、Cu recess 控制、CMP、表面活化、缺陷检测、可靠性与可路由 test vehicle；这属于技术路线机会，不能直接写入当期市场销售额。
3. **TSV/背面连接机会：** nTSV/TDV、背面光刻、减薄、形变补偿与检测；其应用口径必须与传统 TSV、HBM TSV、2.5D interposer TSV 和 W2W HB 分开。

要把任一技术指标转换为销量、产能或成本，至少需要产品状态、有效 I/O、良率/可靠性、稼动率、产品 mix、单位定义和商业交付七项公开证据。详见 [evidence-gaps.md](./evidence-gaps.md)。
