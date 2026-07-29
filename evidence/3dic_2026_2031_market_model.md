# A组：2026—2031年3D IC市场规模、销售额与三情景模型

**资料截点：2026-07-29｜单位：十亿美元（USD bn），另有说明除外｜模型标签：A6**

> **结论先行。** 公开披露无法给出一张可审计的“全球3D IC收入表”：Sony、TSMC、Intel、Samsung、HBM三厂和设备商均没有按同一3D IC定义拆出收入、单位出货与有效产能。因此，本组拒绝把全部先进封装、CoWoS总产能、HBM销售额或厂商总收入当作3D IC市场实际值；以下绝对额是以产品商业状态、厂商收入/订单和第三方方向预测校准的 **A6情景模型**。基准情景下，狭义3D IC制造/封装服务收入由2026年约 **$14.0bn** 增至2031年 **$36.5bn**，五年CAGR **21.1%**；相关设备材料增量由 **$4.3bn** 增至 **$11.7bn**，CAGR **22.2%**；搭载3D IC的终端半导体价值池由 **$150bn** 增至 **$335bn**，CAGR **17.4%**。三层不可相加，后两层更不能冒充第一层销售额。

## 1. 口径：三层价值必须分开

| 层级 | 本组定义 | 计入 | 明确排除 |
|---|---|---|---|
| **M1 狭义3D IC制造/封装服务收入** | 具备垂直功能集成的堆叠结构所对应的增量制造、键合、堆叠、组装与测试服务价值 | stacked CIS键合/集成、array—CMOS分离型3D NAND的晶圆集成价值、TSV堆叠HBM的堆叠/测试价值、logic-on-cache、logic-on-logic、active/functional die 3D、选择性CPO/MEMS 3D | 纯2.5D中介层、普通fan-out/FC-BGA/PoP、全部CoWoS、逻辑裸晶/HBM DRAM本体、设备材料收入 |
| **M2 相关设备材料增量** | 因3D堆叠而增加的CMP、清洗/活化、沉积/电镀、键合、临时键合/解键合、薄化、检测、KGD/系统测试、特种材料收入 | 只计与3D工艺强相关的可服务增量 | Applied、Lam、KLA、Besi、SUSS等公司总收入；客户产品价值 |
| **M3 搭载3D IC的终端半导体价值池** | 包含至少一项本报告狭义3D结构的可售半导体产品价值 | stacked CIS、相关3D NAND、HBM stack、3D cache/logic产品、相应AI/HPC模块中可归属的半导体内容 | 服务器/手机整机、云CapEx、数据中心建筑/网络/液冷，以及不含3D结构的全部芯片 |

**边界提醒。** HBM本身是TSV堆叠3D存储，但GPU+HBM的CoWoS系统总体是2.5D；本组只把HBM stack内部的3D堆叠/测试服务计入M1，把HBM器件销售额计入M3，不把CoWoS中介层总加工额整体计入M1。Hybrid bonding是3D IC的一种互连实现，并非3D IC全集；HBM4也不自动等于hybrid bonding。

## 2. 证据分层：哪些是事实，哪些只是预测

| 标签 | 类型 | 本组可确认内容 | 不能据此确认 |
|---|---|---|---|
| **A1 实际值** | 经审计财报/正式业绩 | Besi FY2025收入€591.3m、订单€685.0m、Q4订单€250.4m；NVIDIA FY2025数据中心收入$115.2bn、Blackwell FY25 Q4收入$11bn；AMD 2024 Instinct收入超过$5bn；Sony I&SS及设备商存在实际商业收入 | 按3D IC/hybrid bonding拆分的产品收入、全球die/wafer出货 |
| **A2 公司指引/状态** | 公司产品页、路线图、量产/准备声明 | TSMC SoIC/3DFabric、Intel Foveros Direct、Samsung X-Cube、Sony stacked CIS、AMD 3D V-Cache、SK hynix/Micron/Samsung HBM路线存在 | 统一有效WPM、良率、客户单位采购量、未来全球销售额 |
| **A5 第三方预测** | TrendForce、Yole、SEMI、IDC等 | AI/HPC、HBM、先进封装增长方向；例如TrendForce给出2025 CoWoS超过75k wafers/month的供应链估计 | 狭义3D IC的同口径实际销售额；CoWoS WPM不能变成SoIC/HB WPM |
| **A6 本报告模型** | 本组显式假设、情景与计算 | 下列2026—2031三层价值、应用拆分、容量指数 | 公司承诺、订单、实际出货或投资建议中的确定现金流 |

公开付费市场摘要对“3D IC”常分别混入先进封装、TSV、3D NAND器件、EDA或终端芯片，基年/终年也不一致。本组只把它们作为区间与方向校准，不把无法取得完整定义和底表的CAGR升格为事实。

## 3. M1：狭义3D IC制造/封装服务收入

### 3.1 三情景年度销售额

| 年份 | 低情景 | 基准情景 | 高情景 | 基准YoY | 基准驱动 | 基准约束 |
|---|---:|---:|---:|---:|---|---|
| 2026E | 11.0 | **14.0** | 17.0 | — | stacked CIS/NAND存量；HBM3E/4堆叠；SoIC/3D cache商业基线 | 厂商不拆分收入；HBM4并非全面HB |
| 2027E | 12.5 | **17.0** | 22.0 | **21.4%** | AI/XPU与HBM容量提高；logic/cache更多设计导入 | qualification、KGD、热/翘曲、客户集中 |
| 2028E | 14.1 | **20.8** | 28.5 | **22.4%** | 多客户logic-on-logic/cache；部分CPO进入初始收入 | 低良率可能吞噬互连收益；TCB继续竞争 |
| 2029E | 16.1 | **25.3** | 36.8 | **21.6%** | D2W工具/工艺成熟；3D逻辑与HBM stack复杂度增值 | 工具安装到合格产出存在多季度滞后 |
| 2030E | 19.0 | **30.5** | 46.8 | **20.6%** | AI推理、近存/缓存、CPO、区域化OSAT供给 | 终端利用率、电力、CapEx周期与ASP学习曲线 |
| 2031E | 22.5 | **36.5** | 58.5 | **19.7%** | 3D logic/cache成为第二增长极，CIS/NAND继续贡献底盘 | 高端能力仍集中；开放chiplet责任/测试生态不完整 |
| **2026—31 CAGR** | **15.4%** | **21.1%** | **28.0%** |  |  |  |
| **六年累计额** | **95.2** | **144.1** | **209.6** |  |  |  |

低情景不是“行业衰退”，而是CIS/NAND底盘仍增长但HB/logic迁移延迟；高情景要求2027—2029连续出现多客户、跨两个产品周期的可审计量产，而不只是设备订单。

### 3.2 基准情景应用拆分（M1，四舍五入）

| 年份 | stacked CIS | array—CMOS型3D NAND集成 | HBM stack内部堆叠/测试 | logic/cache/logic | CPO/光子3D | MEMS/汽车/边缘 | 其他/研发小量 | 合计 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| 2026 | 4.48 | 3.50 | 2.52 | 1.96 | 0.28 | 0.56 | 0.70 | **14.00** |
| 2027 | 5.10 | 4.08 | 3.23 | 2.55 | 0.43 | 0.68 | 0.94 | **17.01** |
| 2028 | 5.82 | 4.78 | 4.16 | 3.54 | 0.62 | 0.83 | 1.04 | **20.79** |
| 2029 | 6.58 | 5.57 | 5.31 | 4.81 | 1.01 | 1.01 | 1.01 | **25.30** |
| 2030 | 7.32 | 6.40 | 6.71 | 6.40 | 1.53 | 1.22 | 0.91 | **30.49** |
| 2031 | 8.03 | 7.30 | 8.03 | 8.39 | 2.56 | 1.46 | 0.73 | **36.50** |

**结构变化。** CIS仍是最成熟应用，但基准占比从32%降至22%；3D NAND从25%降至20%；HBM堆叠内部服务从18%升至22%；logic/cache从14%升至23%，在2031成为最大单一增量来源。CPO从2%升至7%，绝对值增长快但仍属高波动期权。上述是A6分配，不是厂商分部收入。

## 4. M2：3D IC相关设备材料增量

| 年份 | 低情景 | 基准情景 | 高情景 | 基准YoY | 主要内容 |
|---|---:|---:|---:|---:|---|
| 2026E | 3.4 | **4.3** | 5.2 | — | 表面/CMP/清洗、键合、薄化、检测与测试安装基线 |
| 2027E | 3.8 | **5.2** | 6.7 | **20.9%** | D2W/W2W设备交付与客户验收 |
| 2028E | 4.5 | **6.3** | 8.7 | **21.2%** | recipe与计量闭环、复购和区域化供应 |
| 2029E | 5.2 | **7.7** | 11.1 | **22.2%** | overlay/void/颗粒检测、KGD和系统级测试提升 |
| 2030E | 6.0 | **9.5** | 14.2 | **23.4%** | logic 3D与CPO放量带来更高测试/材料强度 |
| 2031E | 7.0 | **11.7** | 18.0 | **23.2%** | 工艺从单机竞争转为成套良率解决方案 |
| **2026—31 CAGR** | **15.5%** | **22.2%** | **28.2%** |  |  |
| **六年累计额** | **29.9** | **44.7** | **63.9** |  |  |

该模型不是“设备商总营收”之和。2026基准可理解为：全球半导体设备材料大盘中，能够由3D堆叠新增工序合理归属的服务可用增量。Besi的真实订单/收入证明需求存在，却无法拆出键合设备单项；EVG为私营公司，公开组合可确认能力但未披露可审计收入。M2的价值捕获较M1前置约2—6个季度，但产品收入还需安装、验收、recipe、qualification和良率爬坡。

## 5. M3：搭载3D IC的终端半导体价值池

| 年份 | 低情景 | 基准情景 | 高情景 | 基准YoY | 基准解释 |
|---|---:|---:|---:|---:|---|
| 2026E | 125 | **150** | 180 | — | 以CIS、3D NAND、HBM及少量3D逻辑产品器件价值为主 |
| 2027E | 140 | **175** | 218 | **16.7%** | HBM4平台、AI ASIC与logic/cache扩张 |
| 2028E | 158 | **207** | 264 | **18.3%** | 每模块存储价值上升，多客户AI和3D逻辑导入 |
| 2029E | 180 | **245** | 320 | **18.4%** | 推理需求、CPO初量、NAND周期回升假设 |
| 2030E | 210 | **288** | 390 | **17.6%** | 更高容量HBM、3D cache/logic与高端感知 |
| 2031E | 245 | **335** | 480 | **16.3%** | 终端产品价值扩张，但不包含整机/云服务收入 |
| **2026—31 CAGR** | **14.4%** | **17.4%** | **21.7%** |  |  |
| **六年累计额** | **1,058** | **1,400** | **1,852** |  |  |

M3的绝对额最大，是因为包含DRAM/NAND/CIS/逻辑器件价值；它不是封装厂或设备商的可得收入。尤其不能把NVIDIA数据中心收入、云厂商CapEx或整机机柜ASP装入M3。

## 6. 容量：不用伪精确WPM，采用“披露值 + 有效能力指数”双轨

### 6.1 已披露物理产能

| 领域/厂商 | 可审计3D/HB有效WPM | 本组处理 |
|---|---:|---|
| TSMC SoIC、Intel Foveros Direct、Samsung X-Cube/直接键合 | **未披露统一有效WPM** | 不以总封装或CoWoS WPM替代 |
| Sony stacked CIS direct-bond产能 | **未按Cu–Cu/direct-bond拆分** | 不以I&SS收入或全部sensor出货替代 |
| HBM三厂 | 公布产品/路线、部分sold-out或准备状态，但未形成同口径“合格3D stack WPM” | 不以DRAM总WPM或HBM销售额反推 |
| YMTC、新芯股份等中国平台 | 未披露同口径HB有效WPM | 平台存在不等于稳定合格产出 |
| Besi、EVG、SUSS、ASMPT | 设备商，不拥有客户产品WPM | 订单只作领先指标 |

### 6.2 A6有效能力指数（2026基准=100）

“有效能力”要求设备已安装验收、recipe闭环、产品通过qualification并达到可重复良率；并非名义tool throughput。

| 年份 | 低情景 | 基准情景 | 高情景 | 基准YoY | 解释 |
|---|---:|---:|---:|---:|---|
| 2026 | 100 | **100** | 100 | — | 基准年 |
| 2027 | 110 | **120** | 132 | **20.0%** | 2025—26工具订单转为部分合格能力 |
| 2028 | 121 | **147** | 176 | **22.5%** | D2W对准/良率与测试闭环改善 |
| 2029 | 135 | **180** | 233 | **22.4%** | 多客户量产、区域OSAT参与 |
| 2030 | 153 | **220** | 303 | **22.2%** | logic/cache、HBM复杂度与CPO需求 |
| 2031 | 174 | **265** | 390 | **20.5%** | 基准五年2.65倍；高情景需跨产品周期证明 |
| **CAGR** | **11.7%** | **21.5%** | **31.3%** |  |  |

收入可以跑赢/跑输能力指数：早期复杂度、低良率和高测试强度抬高每单位服务价值；成熟后学习曲线压低ASP。故不能把容量指数线性换算为wafer或die销量。

## 7. 模型假设、敏感性与可证伪触发器

| 变量 | 低情景 | 基准情景 | 高情景 | 可证伪观测 |
|---|---|---|---|---|
| AI/HBM需求 | CapEx回撤、利用率/电力限制 | 推理增长吸收新增供给，HBM4按代际爬坡 | 多个ASIC与GPU平台同时超预期 | CSP CapEx中的服务器比例、HBM客户认证、实际交期/库存 |
| Hybrid bonding迁移 | TCB/micro-bump持续满足大多数需求 | CIS/logic-cache先行，HBM精选导入 | 16-high及逻辑3D快速迁移 | 命名SKU截面/官方BOM、客户量产、hybrid bonder复购 |
| 良率/KGD | 良率窗口反复，报废抵消性能收益 | 2027—29跨两代产品闭环 | 多供应商达到可互换稳定良率 | wafer/die良率、void/overlay、burn-in与现场失效率披露 |
| 设备与材料 | 工具订单取消/验收延期 | 订单后2—6季度变为合格产能 | 成套工艺复购、区域扩产同步 | 订单—收入—验收—客户产品收入的完整链条 |
| 竞争与价格 | 需求弱、ASP学习曲线快 | 复杂度增值大致抵消单工序降价 | 供给紧缺、定制流程溢价 | OSAT/foundry先进封装毛利、交期、利用率 |
| CPO | 2030前仍小量 | 2028初始收入、2030后扩大 | 2027已有多家系统客户批量 | 可售光引擎/交换机量、可靠性与封装供应链公告 |

**模型误差管理。** M1/M2绝对额应按至少±25%管理，M3按±20—30%管理；情景区间不是统计置信区间。以下事件发生时必须重估：①两家以上头部厂商披露同口径3D/HB收入或有效WPM；②命名HBM4/4E SKU正式确认hybrid bonding并出现批量收入；③logic-on-logic连续两个客户产品周期量产；④AI CapEx连续两个季度同比下修超过20%；⑤HBM/先进封装交期回到成熟品水平且利用率明显下降。

## 8. 商业机会排序：谁能捕获利润

| 机会 | 2026—31价值判断 | 收入时点 | 主要玩家/角色 | 核心门槛 |
|---|---|---|---|---|
| **KGD/KGW、DFT、burn-in和高速测试** | **最高确定性之一**；多die价值越高，测试损失成本越大 | 随HBM/logic 3D同步 | Advantest、Teradyne、KLA及OSAT测试团队 | 可测试性IP、并行度、热/高速信号与数据闭环 |
| **CMP、清洗活化、表面/颗粒/void计量** | HB不可绕过，且良率决定商业闭环 | 设备订单领先产品收入 | Applied、EBARA、Entegris、KLA、国产CMP/清洗/检测链 | 亚纳米表面、Cu recess、污染控制、现场协同 |
| **D2W高精度键合与临时键合/解键合** | logic/cache和KGD驱动，价值密度高 | 2027—29导入加速 | Besi、EVG、SUSS、ASMPT等 | overlay、吞吐、良率、薄晶圆搬运和客户服务 |
| **3D EDA/PDK、热/应力/PDN、DFT IP** | 轻资产、高锁定；开放chiplet落地的必要层 | 设计导入领先量产2—4年 | Synopsys、Cadence、Siemens、foundry生态/IP商 | 跨厂规则、sign-off、责任边界和数据保密 |
| **W2W/D2W制造服务与OSAT区域化** | M1最大直接收入池；但CapEx和客户认证重 | 2027后多客户形成收入曲线 | TSMC、Intel、Samsung、Sony、ASE、Amkor、JCET及区域厂 | 先进节点协同、良率、热/测试、长期客户承诺 |
| **CPO/电子—光子3D集成** | 高上行期权，短期不宜高估 | 2028初始、2030后可能加速 | foundry、光引擎、交换ASIC、OSAT | 激光/耦合、可靠性、可测试性与系统成本 |
| **中国设备材料替代** | 从单点设备转向成套recipe/计量闭环才可捕获利润 | 2026—29验证，后续复购 | CMP、清洗、电镀、薄化、检测、键合与测试厂商 | 客户验证、持续服务、耗材一致性；不能只看样机 |
| **算苗/中科声龙相关3D存算** | 技术路线有专利支撑，但商业收入仍属期权 | 需经过流片—点亮—封装—客户认证—量产门 | 定制存储晶圆、Buffer Die、3D测试和封装伙伴 | 截至截点无公开良率、供应商、单位出货；160GB/16TB/s不得进实际值 |

## 9. 至少20条公开来源及使用边界

| # | 来源 | 类型/用途 | 边界 |
|---:|---|---|---|
| 1 | [TSMC 3DFabric](https://www.tsmc.com/english/dedicatedFoundry/technology/3DFabric) | A2，SoIC/CoWoS/InFO平台 | 无SoIC收入、客户WPM |
| 2 | [TSMC HPC Wafer-Level System Integration](https://www.tsmc.com/english/dedicatedFoundry/technology/platform_HPC_tech_WLSI) | A2，HPC集成路线 | 不证明具体SKU出货 |
| 3 | [Intel Advanced Packaging](https://www.intel.com/content/www/us/en/foundry/advanced-packaging.html) | A2，Foveros/Direct/EMIB | 无各平台外部客户量 |
| 4 | [Samsung Foundry Advanced Packaging](https://semiconductor.samsung.com/foundry/advanced-packaging/) | A2，X/I/H-Cube | 2.5D与3D须分开 |
| 5 | [Sony 2-Layer Transistor Pixel公告](https://www.sony-semicon.com/en/info/2021/202112/20211215.html) | A2/A4，stacked CIS技术 | 无按Cu–Cu拆分出货 |
| 6 | [Sony stacked CMOS技术](https://www.sony-semicon.com/en/technology/mobile/stacked-cmos.html) | A2/A4，成熟应用 | 无统一pitch/收入 |
| 7 | [AMD 3D Chiplet](https://www.amd.com/en/corporate/events/3d-chiplet.html) | A2，3D V-Cache产品路线 | CPU收入不等于HB服务收入 |
| 8 | [AMD EPYC 3D V-Cache](https://www.amd.com/en/newsroom/press-releases/2022-3-21-amd-epyc-processors-with-amd-3d-v-cache-technol.html) | A2，可售逻辑—缓存例 | 无封装服务拆分 |
| 9 | [YMTC Xtacking](https://www.ymtc.com/en/technology/xtacking) | A2，array/periphery分离路线 | 每代互连须逐品核验 |
| 10 | [Kioxia BiCS FLASH](https://www.kioxia.com/en-jp/business/technology/bics-flash.html) | A2，3D NAND路线 | 不能自动归为HB |
| 11 | [Samsung V-NAND/COPS](https://semiconductor.samsung.com/newsroom/tech-blog/the-technology-behind-samsungs-8th-generation-v-nand/) | A2，单晶圆COPS对照 | COPS不等于W2W HB |
| 12 | [SK hynix 2025 Q1业绩](https://news.skhynix.com/sk-hynix-announces-first-quarter-2025-financial-results/) | A1/A2，HBM需求/路线 | sold out不等于交付量 |
| 13 | [Micron FY2025 Q2业绩](https://investors.micron.com/news-releases/news-release-details/micron-technology-inc-reports-results-second-quarter-fiscal-2025) | A1/A2，HBM3E/4节奏 | 无HB工艺拆分 |
| 14 | [Samsung HBM](https://semiconductor.samsung.com/dram/hbm/) | A2，产品路线 | HBM4不等于HB |
| 15 | [Besi FY2025业绩](https://www.besi.com/investor-relations/press-releases/details/be-semiconductor-industries-nv-announces-q4-25-and-full-year-2025-results/) | A1，收入/订单实际值 | 无HB工具/客户拆分 |
| 16 | [EV Group](https://www.evgroup.com/) | A2，键合/计量组合 | 私营；无审计收入/安装量 |
| 17 | [SUSS IR News](https://www.suss.com/en/investor-relations/news/) | A1/A2，经营和产品 | 无direct-bond收入拆分 |
| 18 | [ASMPT Financial Reports](https://www.asmpt.com/investor-relations/financial-reports/) | A1，设备经营 | 总收入不能推3D量 |
| 19 | [Applied Materials FY2024](https://ir.appliedmaterials.com/news-releases/news-release-details/applied-materials-announces-fourth-quarter-and-fiscal-year-2024-results) | A1，材料工程设备商业规模 | 不能拆出HB CMP收入 |
| 20 | [Lam Research FY2025](https://newsroom.lamresearch.com/2025-07-30-Lam-Research-Corporation-Reports-Financial-Results-for-the-Quarter-Ended-June-29,-2025) | A1，晶圆设备实际收入 | 无3D专用拆分 |
| 21 | [DISCO IR](https://www.disco.co.jp/eg/ir/financial_information/) | A1，薄化/切割设备 | 总收入不等于3D增量 |
| 22 | [KLA FY2025](https://ir.kla.com/news-releases/news-release-details/kla-corporation-announces-fourth-quarter-and-fiscal-year-2025-results) | A1，过程控制商业规模 | 无HB检测拆分 |
| 23 | [Advantest FY2024](https://investor.advantest.com/en/ir/news/2025/20250425.html) | A1，测试市场代理 | 无3D专用收入 |
| 24 | [TrendForce HBM需求预测](https://www.trendforce.com/presscenter/news/20240506-12125.html) | A5，HBM需求方向 | 预测非实际出货；非HB市场 |
| 25 | [TrendForce 2025 CoWoS产能报道](https://www.trendforce.com/news/2025/01/02/news-tsmc-set-to-expand-cowos-capacity-to-record-75000-wafers-in-2025-doubling-2024-output/) | A5，供应紧张/扩产代理 | CoWoS WPM非SoIC WPM |
| 26 | [Yole Advanced Packaging Market Monitor 2024](https://www.yolegroup.com/product/report/advanced-packaging-market-monitor-2024/) | A5，方法与AI/HPC方向 | 付费底表不可见；先进封装非M1 |
| 27 | [SEMI Advanced Packaging](https://www.semi.org/en/advanced-packaging) | A5，行业入口/资本设备方向 | 不提供同口径实际3D收入 |
| 28 | [NVIDIA FY2025业绩](https://nvidianews.nvidia.com/news/nvidia-announces-financial-results-for-fourth-quarter-and-fiscal-2025) | A1，终端AI需求实际收入 | 不能除ASP推3D数量 |
| 29 | [AMD 2024业绩](https://ir.amd.com/news-events/press-releases/detail/1228/amd-reports-fourth-quarter-and-full-year-2024-financial-results) | A1，Instinct收入锚 | 不等于HBM/封装服务收入 |
| 30 | [Adeia DBI](https://adeia.com/semiconductor/inventing-connections-for-humanity) | A2，direct-bond IP生态 | IP平台不证明客户量产数 |
| 31 | [新芯股份三维集成平台](https://www.xmcwh.com/site/3D-IC-platform) | A2，中国TSV/HB平台能力 | 无有效WPM、客户、良率 |
| 32 | [算苗A4E实名发布稿](https://www.sohu.com/a/1037905760_122593914) | A2，公司宣称流片/8层/16TB/s | 不证明完成封装或出货 |
| 33 | [CN121920305A](https://patents.google.com/patent/CN121920305A/zh) | A4，算苗计算—存储HB权利要求 | 专利非产品采用/量产 |
| 34 | [CN219040074U](https://patents.google.com/patent/CN219040074U/zh) | A4，中科声龙存储—计算HB设计 | 已转让新加坡声龙；非算苗资产 |

## 10. 可直接进入主报告的A组裁决

1. 2026是模型基准年，2031是五年后的预测终点；表中六个自然年度并不矛盾。
2. 基准M1收入五年CAGR为21.1%，但成长并非直线：2027—29为logic/cache、HBM复杂度和设备转产能的主要斜率窗口，2030—31增速略降但价值池仍扩大。
3. “市场很大”的真正含义分三层：2031基准M1约$36.5bn、M2约$11.7bn、M3约$335bn；三者不能相加或互相替代。
4. 全球3D/HB有效WPM仍不可审计。主报告应使用2026=100的有效能力指数，并把任何厂商WPM留给有明确工艺、地点、时间、良率定义的原始披露。
5. 未来五年最优商业机会不只在键合机，而在良率闭环：CMP/清洗/表面计量、D2W对准、薄晶圆处理、void/overlay检查、KGD/burn-in、高速测试、3D EDA/PDK、热/PDN和可追溯数据。
6. 算苗/中科声龙只进入机会监测，不进入实际销售额：专利支撑设计路线，A4E公开信息仍不支撑量产、客户验收或单位出货。
