# Hybrid Bonding 商业、市场与产能研究｜D组：实际账本、爬坡、渗透与2031情景

**版本与截止日：** v1，2026-07-28。  
**研究目的：** 判断 hybrid bonding（Cu–Cu/介质直接键合）的商业化究竟走到哪里、哪些数据可以称为实际发生、哪些只是设备需求或未来规划，以及 2025—2031 的合理渗透路径。  
**纪律：** 不用总厂 WPM、封测厂总营收、厂房面积、CapEx、设备订单或服务器/GPU收入反推 hybrid-bonded wafer、die、HBM stack或package数。公开没有统一物理产量时，宁可留空。

---

## 1. 先给结论

1. **截至观察日，最坚实的商业事实在设备侧，不在“全球 hybrid-bonded die 出货”侧。** Besi FY2025收入和订单、SUSS/ASMPT/Applied/TEL/Lam等公司的正式财报，证明先进封装与前道装备正在形成真实收入；它们不能量化下游 Cu–Cu 键合产品出货。
2. **真正有成熟大规模商业产品基础的 hybrid bonding 首先来自 CIS/图像传感器的晶圆级堆叠与部分逻辑—缓存/异构集成，而不是已经公开可审计的 AI/HBM 大宗产品。** Sony、TSMC、Intel、Samsung 等都具备不同形式的3D/先进封装平台或产品路线，但企业普遍不披露“Cu–Cu hybrid-bonded wafer/die 的季度单位数、有效 WPM、客户产品与良率”。
3. **HBM、TSV+bump/TCB与 hybrid bonding 将并行至2031。** HBM4的高 I/O、base-die、功耗和系统认证推动更高密度互连需求，但没有公开事实支持“HBM4=全面Cu–Cu direct bond”或“HBM4产量=hybrid bonding产量”。
4. **2025—2027 是验证与首次关键设计导入窗口；2028—2031 才可能从影像/特殊3D逻辑扩大到高端逻辑—缓存、部分CPO和精选的内存—逻辑近存产品。** 这是 B6 本组情景判断，而不是厂商销售指引。其最大变量不是键合机标称吞吐，而是 KGD、表面/粒子控制、可靠性、测试、热与客户系统认证。

---

## 2. 标签与“产能”的六层定义

| 标签 | 含义 | 可用于什么 | 禁止推导 |
|---|---|---|---|
| **D1 实际收入/实物交付** | 年报、季报或正式业绩新闻中确认的设备、材料、产品收入/交付 | 厂商自身商业化规模 | 下游产品 die/HBM/封装数（除非该单位被披露） |
| **D2 已量产/可售/产品平台** | 公司正式宣布 mass production、commercial availability、产品/平台能力 | 产品或工艺进入可售/量产状态 | 满产、有效产能、客户份额和销量 |
| **D3 建设/扩产/投资计划** | 开工、投资、设备购置、未来产能目标 | 未来供给意图 | 当前产能或当前出货 |
| **D4 技术论文/演示/专利** | 技术参数、实验线、路线图 | 工艺能力和可能性 | 客户订单、稳定良率与商业规模 |
| **D5 第三方研究/媒体** | TrendForce、Yole、Reuters、EE Times等 | 供需旁证或预测 | 公司事实、实际产量 |
| **D6 本组情景** | 公式、假设、敏感性 | 方向和压力测试 | 事实账本、市场份额或厂商承诺 |

产能必须再分：

1. **设计/铭牌产能**：厂房或工具理论上限；
2. **已装机产能**：工具在厂，不等于工艺验收；
3. **认证可用产能**：通过客户/内部 qualification；
4. **有效产能**：考虑良率、产品组合、返工、测试和瓶颈后的可生产能力；
5. **实际产出/出货**：某期间真实完成的 wafer/die/package或收入；
6. **利用率**：实际投入/产出相对有效能力。

没有公司逐层披露时，“W2W/D2W有效产能”应写作**未披露**。设备台数、厂房投资或第三方的总封装 WPM，均无法替代第五层。

---

## 3. 设备商业化：收入与订单是最强可验证数据，但不等于产品出货

### 3.1 事实账本

| 厂商 | 公开事实 | 标签 | 可以得出的结论 | 明确不可得/不可推 |
|---|---|---|---|---|
| **Besi** | FY2025收入 **€591.3m**，全年订单 **€685.0m**，Q4订单 **€250.4m**；公司将订单改善部分联系到亚洲 OSAT 的 2.5D AI、光子及 hybrid-bonding 需求。 | D1 | 先进封装/混合键合装备需求已体现在 Besi 自身订单与收入。 | 客户名单、每类工具数、验收、W2W/D2W占比、实际键合die/wafer、HBM stack与任何客户份额。 |
| **Applied Materials** | FY2024业绩和10-K确认公司及 Semiconductor Systems 等分部已实现收入。 | D1 | 沉积、CMP、材料工程、封装互连等资本设备有真实商业规模。 | 从分部收入拆出的 hybrid-bond CMP/沉积/电镀设备收入，或下游产品产能。 |
| **SUSS MicroTec** | FY2024业绩新闻披露收入/订单；产品组合含先进封装光刻、对准、键合、临时键合/解键合等。 | D1+D2 | 公司有实际装备经营及可服务先进封装/3D的产品组合。 | Cu–Cu直接键合产品量、客户工具数、实际WPM、稳定良率。 |
| **ASMPT** | 年报披露半导体解决方案/SMT合并经营；组合覆盖 die bonding、封装装配、molding和检查。 | D1+D2 | 后段装备与自动化具实际商业收入。 | 其总营收中 direct-bond/先进封装份额、下游产品出货。 |
| **EV Group（EVG）** | 私营公司官方组合覆盖 wafer bonding、alignment、temporary bonding/debonding、metrology和heterogeneous integration。 | D2/D4 | EVG 是 W2W/D2W、临时键合与计量的核心设备参与者。 | 未公开可审计总收入、订单、客户工具数、有效WPM或die出货。 |
| **TEL / Lam / DISCO / KLA / Advantest** | 各自财报确认订单、系统销售、磨削切割、过程控制、测试系统等实际商业收入。 | D1 | TSV、减薄、缺陷控制、KGD/高速测试等瓶颈环节有真实资本设备市场。 | 用总设备收入折算 hybrid-bond产能、产品出货或客户指定需求。 |

### 3.2 设备订单的滞后链条

```text
设备订单（D1）
  → 制造/交付（通常数月，未必公开）
  → 厂内安装与验收（数月，客户保密）
  → 材料/recipe/计量闭环（多季度）
  → 客户产品 qualification（多季度）
  → 稳定良率、测试覆盖和成本爬坡（可能跨1—2个产品周期）
  → 产品实际出货（需要D1产品收入/实物证据）
```

“工具出货较快、产品爬坡较慢”是D6行业经验，而非任何厂商承诺。直接键合增加的关键阶段是 CMP/清洗/对准/键合/后键合检测之间的协同；一个工具订单更像未来资格认证的领先指标，不能加入当前产品产能。

---

## 4. 量产产品、代理信号与有效产能：哪些能确认，哪些必须留白

### 4.1 可确认的产品/平台状态

| 公司/类别 | 公开状态 | 标签 | 正确解读 | 不能写成 |
|---|---|---|---|---|
| **Sony Semiconductor Solutions / stacked CIS** | Sony长期公开堆叠式CMOS图像传感器产品与技术路线；其业务财报披露 Imaging & Sensing segment等商业收入。 | D1（分部收入）+D2（产品） | 证明晶圆级堆叠/3D集成已经进入大规模消费电子商业场景，是 hybrid bonding 最有说服力的产品类别之一。 | Sony未统一公开 Cu–Cu 绑定的季度die/wafer数、所有产品工艺与有效产能；不将分部收入等同direct-bond出货。 |
| **TSMC / SoIC、3DFabric** | TSMC官方把 SoIC、CoWoS、InFO归入3DFabric；SoIC是其3D集成平台的一部分。 | D2 | 证明领先代工厂提供3D集成/先进封装平台并持续推进规格。 | 未披露 SoIC/Cu–Cu 各客户WPM、die数、良率、收入或AI/HBM拆分。 |
| **Intel / Foveros、EMIB、Foveros Direct** | Intel Foundry公开 Foveros/EMIB和Foveros Direct等平台/路线信息。 | D2/D4 | 证明Intel具备多类3D/2.5D异构集成路线，direct interconnect在路线图中存在。 | 未披露各平台的W2W/D2W实际单位、外部客户产能或Cu–Cu产品出货。 |
| **Samsung / X-Cube、I-Cube和先进封装路线** | Samsung Foundry/semiconductor公开 X-Cube、I-Cube等3D/2.5D平台以及HBM产品/路线资料。 | D2 | 证明其全栈参与3D逻辑、HBM和封装生态。 | 不能据此认定HBM4已全面Cu–Cu hybrid bonding、也无统一有效WPM披露。 |
| **SK hynix / HBM4路线** | 公司宣称完成HBM4开发、准备量产；HBM产品路线由公司持续发布。 | D2（产品准备/状态） | 可作为下一代高I/O存储/封装协同需求的信号。 | 不能把“ready for mass production”理解为已实际HBM4销量，也不能等同hybrid bonding。 |
| **YMTC / 新芯股份（武汉）** | YMTC为3D NAND制造商；新芯股份当前官网的“三维集成工艺平台”页面明确列出TSV、Hybrid Bonding、双/多晶圆堆叠和芯片—晶圆异构集成。 | D2（企业/产品平台） | 只可列为不同主体的中国3D NAND与三维集成能力参与者。 | 不合并两家公司；不使用旧简称或新闻拼接主体；未披露Cu–Cu产品、有效WPM、客户、良率或AI memory stack关系的字段全部留空。 |

### 4.2 “量产产品出货代理数据”的正确层级

产品实物单位的公开性从高到低一般为：

1. 公司明确给出 wafer/die/模组/传感器出货数量（本研究多数公司未给）；
2. 产品线收入或分部收入（可证明商业规模，不能换算单位）；
3. 正式量产/GA/可售状态（可证明产品处于商业可用阶段，不能量化）；
4. 工具订单/安装、CapEx、厂房项目（仅是供给意图或装备周期）；
5. 署名媒体预测和供应链消息（只能旁证）。

因此，本组的“产品出货代理表”只使用收入和可售状态，刻意不输出 pseudo-precision：

| 代理指标 | 例子 | 可以支持 | 不可支持 |
|---|---|---|---|
| 产品/分部收入 | Sony I&SS、先进封装设备收入、TSMC总营收/平台收入若披露 | 相关产品/业务已产生商业收入 | 具体Cu–Cu die、wafer、stack、客户占比 |
| 平台/产品量产声明 | TSMC SoIC/3DFabric、Intel Foveros、Samsung X-Cube、HBM产品声明 | 工艺/平台已进入产品化或量产准备 | 有效WPM、良率、产品销量 |
| AI客户的收入/系统GA | NVIDIA/AMD数据中心收入、云实例GA | 终端AI系统需求是真实商业需求 | hybrid-bond内容、封装供应商和存储数量 |
| 设备订单/收入 | Besi、测试/量测/薄化设备商财报 | 未来工艺资本开支与需求方向 | 下游产品的实际产能/出货 |

---

## 5. W2W/D2W有效产能、扩产项目和爬坡：可以表述的只有这些

### 5.1 产能表

| 参与者 | 公开W2W/D2W产能数字 | 已知建设/扩产状态 | 证据等级 | 报告处理 |
|---|---:|---|---|---|
| TSMC SoIC/3DFabric | **未披露统一、可审计的W2W/D2W有效WPM** | 持续发布3DFabric/SoIC平台与规格；个别3DFabric规格有产品路线信息。 | D2 | 不采用第三方CoWoS WPM代替SoIC/Cu–Cu产能；CoWoS和SoIC不是同一单位/工艺。 |
| Intel Foundry | **未披露** | Foveros/EMIB/Foveros Direct平台/路线持续推进。 | D2/D4 | 不用Intel总封装/晶圆制造能力或Foundry CapEx推direct-bond有效WPM。 |
| Samsung | **未披露** | X-Cube/I-Cube/HBM路线持续发布。 | D2 | 不将HBM或DRAM Fab产能变成hybrid-bond产能。 |
| Sony | **未披露** | 传感器业务持续投资和产品迭代。 | D1/D2/D3（需按单个项目公告核对） | 不以I&SS分部收入或总sensor产量倒推Cu–Cu WPM。 |
| Besi/EVG/SUSS/ASMPT | **不适用：设备商，不直接拥有客户产品WPM** | 订单、产品与服务能力是设备供应信号。 | D1/D2 | 不把工具销售写成制造产能。 |
| YMTC / 新芯股份（武汉，分别统计） | **Hybrid Bonding有效WPM均未披露** | YMTC的NAND产品路线与新芯股份的三维集成平台分别存在；后者平台页并未给出Hybrid Bonding专用WPM。 | D2 | 不以NAND层数、总厂WPM、Fab建设或“量产经验”推混合键合有效产能。 |

结论是：公开范围内无法建立“全球W2W/D2W hybrid bonding有效WPM”或“按厂商有效产能份额”的事实表。任何单一数值若没有明确工艺对象（Cu–Cu/介质direct bonding）、产品形态（W2W或D2W）、地点、时间、良率/测试定义，均不应纳入可审计市场规模。

### 5.2 扩产项目应怎样进入模型

| 项目类型 | 正确标签 | 可以写 | 不可写 |
|---|---|---|---|
| 设备商新增制造/服务能力 | D3 | 设备交付能力可能增加，支持订单兑现 | 客户产品WPM/出货已经增加 |
| 晶圆厂/OSAT先进封装新厂 | D3 | 厂房/投资/建设与潜在区域化供给 | 当前可售Cu–Cu有效产能或客户量产 |
| 客户送样/qualification | D2或D3 | 技术导入与认证窗口 | 商业量产销量、长期订单 |
| 工具订单或复购 | D1 | 设备侧需求与客户资本开支倾向 | 某产品die/wafer实际出货 |

**装机—认证—爬坡的D6一般区间：** 设备制造/安装约数月；新工艺材料/计量闭环与客户资格认证约2—6个季度；稳定yield、测试覆盖和成本下降常跨1—2个产品周期。直接键合的异常风险包括颗粒 excursion、Cu recess漂移、热应力、薄晶圆翘曲和后段无法返工；因此项目宣布到商业有效产出的时间，通常显著长于单台工具交期。

---

## 6. 2025—2031渗透趋势与转折点：事实、第三方与本组情景三张表

### 6.1 已发生事实（D1/D2）

| 期间 | 已发生事实 | 对渗透趋势的含义 |
|---|---|---|
| 2025 | Besi FY2025订单/收入表明先进封装、AI/光子和hybrid-bond相关装备需求增强；领先厂商继续发布SoIC/Foveros/X-Cube/3D平台。 | 工艺资本开支与设计导入在升温，不能量化产品单位渗透。 |
| 2025—2026 | HBM4样品、开发完成或量产准备等厂商公告显示高I/O memory与下一代加速器正进入认证窗口。 | 为更高密度互连创造需求，但TCB/micro-bump与hybrid bonding仍可并行。 |
| 2026 | 多家中国公司披露W2W/C2W、CMP/减薄、清洗、电镀、检测和先进封装模块能力；但客户/成品良率/实际WPM仍少披露。 | 中国供应链从单点设备材料向工艺链建设推进，商业化需逐客户验证。 |

### 6.2 第三方预测（D5）：只能观察方向

Yole、TechInsights、SEMI、TrendForce、SemiAnalysis等经常发布先进封装、hybrid bonding、CoWoS、HBM和设备市场预测。由于多数报告是付费内容、预测口径不同，且公开摘要通常没有完整定义和底层数据，本组不把其CAGR、WPM或份额直接写入事实账本。正确用法是：

* 用于识别**方向**：高密度互连、AI加速器、CIS、chiplet、CPO和先进封装资本开支的增长；
* 用于提出需验证的**供给紧张度假说**；
* 不用于填补企业未披露的 W2W/D2W实际产能、客户关系、设备台数和产品出货。

相关公开入口包括：SEMI先进封装资讯（https://www.semi.org/en/advanced-packaging），Yole集团新闻中心（https://www.yolegroup.com/），TrendForce新闻（https://www.trendforce.com/news/），均访问2026-07-28。

### 6.3 本组2025—2031情景（D6，不是预测销量）

本组不创建缺乏物理输入的“全球 hybrid-bonded die 数”或美元市场规模。取而代之，使用一张**渗透阶段情景表**，把“渗透”定义为：在该应用中的新设计开始采用 direct bonding 的程度，而不是所有已售设备的实际产量。

| 年份 | 基准情景：主要商业位置 | 上行情景触发 | 下行情景触发 | 不变的审计要求 |
|---|---|---|---|---|
| 2025 | CIS、既有3D感测/逻辑产品为主；设备订单和新设计导入增强。 | 已命名的 AI/逻辑—缓存大客户发布量产/收入与结构证据。 | 颗粒/良率/供应或客户验证延后。 | 无客户级die/wafer数不填。 |
| 2026 | 逻辑—缓存、部分chiplet/光子和高端AI周边应用进入更多qualification；中国模块设备能力持续验证。 | D2转D1：客户联合量产、工具验收/复购与产品收入出现。 | 工艺窗口、测试/热/成本无法闭合。 | 不将HBM4送样计入出货。 |
| 2027 | 精选高价值逻辑3D/近存产品可进入初始收入期；W2W与D2W按产品并行。 | 多家客户披露稳定良率/可售产品；封装/测试供给配套。 | 需求转弱或TCB/RDL改善延缓直接键合ROI。 | 仅以D1产品收入/实物确认商业规模。 |
| 2028—2029 | 若可靠性与成本验证通过，direct bonding向更多逻辑—缓存、CPO和特定存储—逻辑应用扩大；仍非所有AI封装通用方案。 | 标准化PDK/测试流、可靠材料供应、多客户复购。 | 设备吞吐/成本、不可返工损失和热管理抑制渗透。 | 区分D2量产声明与D1收入/单位。 |
| 2030—2031 | 成熟应用与部分高端HPC/AI/光子产品中形成更深渗透，市场分化：CIS/逻辑3D可能领先，通用HBM仍可能多工艺并存。 | 先进逻辑/内存客户确认wide adoption及可审计商业数据。 | HBM/TCB/微凸点路线成本性能仍占优，或系统需求改变。 | 不能以预测CAGR代替实物账本。 |

这张表的**公式**不是数值预测，而是一个进入门槛逻辑：

```text
某应用的 direct-bond 渗透 =
  （经 D1 收入/单位或 D2 量产确认的采用产品集合）
  / （该应用所有可比产品集合）
```

现实中分子和分母的单位/产品BOM大多未公开，故无法输出可信百分比。只有当逐产品 adoption 与实际出货都可得时，才可把该公式量化；当前应保持为方向情景，而不是伪精确的2031市场份额。

---

## 7. 决定2031竞争格局的转折点与监测清单

| 转折点 | 为什么重要 | 必须看到的证据 | 常见误判 |
|---|---|---|---|
| **从设备订单转向产品D1收入** | 订单只表明资本开支，产品收入才说明商业闭环。 | 客户/代工/封测方对命名产品的收入或单位披露。 | Besi订单=AI hybrid-bond die出货。 |
| **从单点键合转向全链良率** | 直接键合良率受CMP、清洗、对准、薄化、检测、测试共同决定。 | Cu recess/particle/overlay、void、可靠性、KGD、最终yield。 | 键合机精度=量产良率。 |
| **W2W与D2W的产品分工** | W2W可在匹配晶圆上提高吞吐，D2W有die挑选灵活性，但工艺/成本不同。 | 结构图、die尺寸、已知良品策略、工具与良率资料。 | 把任何“3D”统称W2W或Cu–Cu。 |
| **HBM4/5的具体键合选择** | 高I/O促使互连升级，但工艺路径由供应商、base die、热和良率共同决定。 | HBM厂/客户的产品BOM和制造声明。 | HBM4/5必然全用hybrid bonding。 |
| **CIS与AI/HPC的节奏差** | CIS商业化早、规模大；AI/HPC封装价值高但可靠性/热/测试更复杂。 | 按应用分列产品收入、出货、良率与客户导入。 | 用CIS产量证明AI direct-bond市场已经同规模。 |
| **中国链从模块到闭环** | 本土设备材料的实际价值取决于是否完成客户产品/良率/测试验证。 | 型号—客户—验收—量产产品—收入/交付。 | 将相关设备材料企业自动认定为某AI设计公司供应商。 |

---

## 8. 来源索引：一手事实、第三方入口和禁用换算

### 8.1 主要一手来源

1. Besi，FY2025 results，2026-02-19：<https://www.besi.com/investor-relations/press-releases/details/be-semiconductor-industries-nv-announces-q4-25-and-full-year-2025-results/>。
2. Applied Materials，FY2024 results，2024-11-14：<https://ir.appliedmaterials.com/news-releases/news-release-details/applied-materials-announces-fourth-quarter-and-fiscal-year-2024-results>。
3. SUSS MicroTec，IR news：<https://www.suss.com/en/investor-relations/news/>（访问2026-07-28）。
4. ASMPT，financial reports：<https://www.asmpt.com/investor-relations/financial-reports/>（访问2026-07-28）。
5. EV Group，wafer bonding/3D integration产品入口：<https://www.evgroup.com/>（访问2026-07-28）。
6. TEL，earnings library：<https://www.tel.com/ir/library/earnings/>（访问2026-07-28）。
7. Lam Research，FY2025 results，2025-07-30：<https://newsroom.lamresearch.com/2025-07-30-Lam-Research-Corporation-Reports-Financial-Results-for-the-Quarter-Ended-June-29,-2025>。
8. DISCO，financial information：<https://www.disco.co.jp/eg/ir/financial_information/>（访问2026-07-28）。
9. KLA，FY2025 results，2025-07-31：<https://ir.kla.com/news-releases/news-release-details/kla-corporation-announces-fourth-quarter-and-fiscal-year-2025-results>。
10. Advantest，FY2024 results，2025-04-25：<https://investor.advantest.com/en/ir/news/2025/20250425.html>。
11. Sony Group，IR/financial results：<https://www.sony.com/en/SonyInfo/IR/library/presen/er/>（访问2026-07-28）。
12. Sony Semiconductor Solutions，technology/products：<https://www.sony-semicon.com/en/>（访问2026-07-28）。
13. TSMC，3DFabric：<https://www.tsmc.com/english/dedicatedFoundry/technology/3DFabric>（访问2026-07-28）。
14. Intel Foundry Direct Connect，2025-04-29：<https://newsroom.intel.com/intel-foundry/intel-foundry-gathers-customers-partners-outlines-priorities>。
15. Intel advanced packaging：<https://www.intel.com/content/www/us/en/foundry/advanced-packaging.html>（访问2026-07-28）。
16. Samsung Foundry advanced packaging：<https://semiconductor.samsung.com/foundry/advanced-packaging/>（访问2026-07-28）。
17. Samsung HBM：<https://semiconductor.samsung.com/dram/hbm/>（访问2026-07-28）。
18. SK hynix HBM4，2025-09-12：<https://news.skhynix.com/en/sk-hynix-completes-worlds-first-hbm4-development-and-readies-mass-production/>。
19. YMTC官网：<https://www.ymtc.com/en/>（访问2026-07-28）。
20. 新芯股份三维集成工艺平台：<https://www.xmcwh.com/site/3D-IC-platform>（访问2026-07-28）。仅证明页面列示的工艺平台；不证明Hybrid Bonding专用WPM、客户、产品或良率。
21. TSMC 3DFabric HPC：<https://www.tsmc.com/english/dedicatedFoundry/technology/platform_HPC_tech_WLSI>（访问2026-07-28）。

### 8.2 第三方入口（D5，仅观察方向）

* SEMI advanced packaging：<https://www.semi.org/en/advanced-packaging>
* Yole Group news：<https://www.yolegroup.com/>
* TrendForce news：<https://www.trendforce.com/news/>
* IEEE Heterogeneous Integration Roadmap：<https://eps.ieee.org/technology/heterogeneous-integration-roadmap.html>

### 8.3 本报告明确禁用的换算

```text
Besi/EVG/SUSS/Applied/TEL/Lam订单或收入 ÷ 假定设备价格
  ≠ 客户已装机工具数
  ≠ W2W/D2W有效产能
  ≠ hybrid-bonded die或HBM stack出货

TSMC/OSAT总营收、CoWoS总WPM、HBM收入、厂房面积、CapEx
  ≠ SoIC/Cu–Cu W2W/D2W有效WPM
  ≠ hybrid-bond产品出货

HBM4/5产品公告、样品、量产准备
  ≠ hybrid bonding全面使用
  ≠ 实际HBM4/5销量
```

---

## 9. 可进入总报告的D组结论

* Hybrid bonding 的商业数据结构是“**设备收入可见、产品单位出货稀缺、有效产能更稀缺**”。这不是研究不足，而是行业披露现实；报告必须承认。
* 2025—2026的硬事实支持设备需求和设计导入升温，而不能支持精确的全球direct-bond WPM或市场份额。最有代表性的可审计数字是Besi自身收入/订单，不是下游AI/HBM出货。
* 2027以后商业化的最大拐点是出现多家客户的 D1 产品收入/实物交付与D2结构证据，而不是更多“混合键合能力”新闻。若出现明确的产品BOM、客户验收、良率/可靠性和实际收入，才应提高2031渗透情景。
* 对TSMC、Intel、Samsung、Sony、YMTC、XMC等，应评价其平台和工艺位置；在没有逐项产能/产品披露时，**不要制造精确排名或有效WPM**。
* 中国链的机会在于由键合、CMP/减薄、清洗/电镀、量测、测试和材料组成的完整工艺闭环；挑战在于将模块能力转化为客户认证、良率和实际产品收入。任何将其直接与某下游设计公司绑定的说法，均需供应方或客户方一手证据。
