# 混合键合全产业链研究｜B组：设备、材料、工艺、测试与厂务的事实账本

**版本与截止日：** v1，2026-07-28。  
**范围：** 本文的混合键合（hybrid bonding）特指以介质—介质预键合、退火后形成介质键，同时以 Cu–Cu 直接互连为目标的晶圆级或 die-to-wafer 三维集成工艺；它不等同于普通 thermocompression bonding（TCB）、micro-bump、wafer fusion、临时键合，亦不自动等同于 HBM4。  
**数据纪律：** 设备商收入、订单和工具能力均不能转换为 hybrid-bonded die、HBM stack、封装数或客户份额。没有客户同意、产品结构、工具验收、良率和实际产出的闭环时，本报告只写“工艺模块参与者/产品能力”，不写“供应商”或“量产份额”。

---

## 1. 状态分级：把“能做”与“已经规模出货”分开

| 标签 | 证据 | 可以写什么 | 明确不能写什么 |
|---|---|---|---|
| **B1：实物交付/收入确认** | 年报、季报、正式业绩新闻中已实现的工具收入、交付或明确产品收入 | 厂商自身的收入/订单/工具交付 | 下游客户的 hybrid-bonded die、HBM 或封装产量 |
| **B2：产品/客户验证/量产声明** | 厂商官网产品页、客户联合公告、正式验证或量产措辞 | 某装备/材料/工艺存在，或处于客户验证/商业应用 | 满产、稳定良率、客户份额、实际产能，除非同页披露 |
| **B3：建设/扩产/项目** | 政府备案、公司投资公告、厂房/设备建设 | 未来供给意图和建设状态 | 当期有效产能和当前出货 |
| **B4：论文/专利/技术演示** | 技术论文、会议、专利、经审阅演讲 | 可达到的实验/开发能力 | 商用良率、订单和规模交付 |
| **B5：署名媒体/行业研究** | Reuters、EE Times、SEMI、专业媒体或有来源的新闻 | 旁证、监测与待核验线索 | 去掉归因后写成公司事实 |
| **B6：模型或不可复核信息** | 自行计算、论坛、股吧、二次转述 | 仅列待核实假设 | 事实表、市场份额、客户关系和出货结论 |

对每一环节，产能还必须区分：**设计/铭牌能力 → 已装机能力 → 客户认证可用能力 → 考虑良率后的有效能力 → 实际产出/出货 → 利用率**。混合键合的瓶颈常在有效能力而不是工具装机：同一条线的真正上限由晶圆表面、颗粒、Cu recess、overlay、后键合检查、可靠性和成品测试共同决定。

---

## 2. 工艺总图：一颗 Cu–Cu hybrid-bonded 3D 产品实际上需要什么

```text
晶圆/裸片设计与PDK
  → 介质/金属沉积、TSV或背面互连（按架构）
  → Cu electroplating / CMP（全局平坦度、Cu recess）
  → 超纯清洗、表面活化、颗粒/金属污染控制
  → 键合前量测与缺陷筛选
  → W2W 或 D2W 高精度对准与预键合
  → 退火形成介质键与 Cu–Cu 互连
  → 临时键合支撑下的减薄、背面加工、TSV/RDL
  → 解键合、切割、组装/基板/热管理
  → 键合后无损检测、KGD、wafer sort、burn-in、封装后与系统测试
  → 自动物料搬运、超纯厂务、追溯/MES、失效分析
```

**关键认知：** direct bonding 不是“买一台键合机”的单点工艺。若介质和铜表面没有足够平坦、足够洁净且 Cu recess 在可控窗口内，键合机的对准精度不能修复界面缺陷；若键合前的 memory/logic die 不是 KGD，八层或更多层的报废风险会以乘法方式放大；若缺少键合后无损检测和高速测试，带宽宣传也无法转化为可销售的产品规格。

---

## 3. 全球全链条：工艺位置、已披露状态、订单/产能的边界

### 3.1 CMP、清洗、沉积、电镀与表面工程

| 工艺环节 | 全球代表厂商 | 已核验的公开事实 | 状态 | 订单/产能/客户边界 | 对 hybrid bonding 的决定性指标 |
|---|---|---|---|---|---|
| **CMP/平坦化** | Applied Materials、EBARA、荏原、Fujimi、CMC Materials/Entegris 等 | Applied FY2024 业绩可确认其 Semiconductor Systems 等业务的实际收入；其材料工程/CMP 产品组合服务多类半导体制造。Fujimi、Entegris公开 CMP slurry/pad、化学品和材料组合。 | B1（各自公司/分部收入）+ B2（产品） | 公开财报通常不拆为 Cu–Cu CMP；不能以 CMP 分部收入或 pad/slurry 销量推键合晶圆数。 | wafer/die global planarity、局部 Cu recess、roughness、dishing/erosion、颗粒、清洗后表面状态。 |
| **清洗/表面活化** | EV Group、SUSS、Applied、Lam、TEL、SCREEN、SEMES 等 | EVG、SUSS 公开 wafer bonding 前的清洗、活化/临时键合与对准产品；TEL/Lam/Applied产品组合覆盖清洗、刻蚀和表面制备。 | B2/B4 | 一般不公布某客户的表面污染规格、键合界面良率或工具台数。 | 金属/有机残留、颗粒、氧化层、接触角、表面能、干燥水印和队列时间。 |
| **Cu plating/金属与介质沉积** | Applied、TEL、Lam、ASMPT/封装设备及材料商 | Applied/TEL/Lam 的正式财报和产品组合证明其沉积、刻蚀、材料工程业务真实存在；但公司收入覆盖先进逻辑、存储、功率、显示等广泛应用。 | B1 + B2 | 不公开 direct-bond Cu pad、dielectric cap、RDL或TSV fill 的客户/厚度/良率组合。 | 铜填充无空洞、晶粒与退火、阻挡层、低应力介质、厚度均匀性、Cu recess 预算。 |
| **介质、CMP/清洗材料** | Entegris、DuPont、Fujimi、CMC/Entegris、JSR、Dow等 | 材料商可披露产品线/合并收入；个别化学品和抛光材料被用于先进逻辑/封装是材料类别事实。 | B1/B2 | 厂商极少披露“某 hybrid-bond 客户的材料牌号、批次、价格、界面可靠性”。 | SiO₂/低k/SiCN等介质表面、slurry选择性、pad硬度、UPW/清洗液杂质、金属污染与键合强度。 |

**全球事实边界。** Applied、Lam、TEL 的年报能证明设备收入的真实存在，却不能证明其中有多少进入 3D IC；EVG/SUSS 的产品页能证明键合/临时键合平台存在，却不能证明客户已将某一 Cu–Cu 结构稳定量产。混合键合材料的采购也无法从供应商收入反推，因为同一种 slurry、清洗化学品或沉积设备可能进入完全不同的前道产品。

### 3.2 键合、对准、临时键合/解键合、减薄和切割

| 环节 | 厂商 | 可直接引用的公开事实 | 状态 | 不可越过的边界 | 路线图/爬坡含义 |
|---|---|---|---|---|---|
| **W2W/D2W hybrid bonding、对准** | **Besi** | FY2025：收入 **€591.3m**、全年订单 **€685.0m**、Q4订单 **€250.4m**；公司将订单改善与亚洲 OSAT 的2.5D AI、光子及 hybrid-bonding 需求相联系。 | B1（Besi收入/订单） | 未披露每个客户工具数、验收、稼动、direct-bond良率、最终 die 数或 HBM stack。 | 设备订单可前瞻资本开支，但从装机、工艺窗口、产品 qualification 到稳定量产通常跨多个季度。 |
| | **EV Group (EVG)** | EVG官方产品组合覆盖 wafer bonding、alignment、temporary bonding/debonding、metrology 与 heterogeneous integration。 | B2/B4 | 私营公司公开资料缺少按 hybrid-bond 的收入、客户、交付台数、实际产能。 | 其角色是前清洗/活化、键合、临时键合和计量的工艺整合；“有平台”不等于某客户量产。 |
| | **SUSS MicroTec** | 公司公开先进封装光刻、对准、键合、临时键合/解键合及清洗/开发平台；FY2024业绩新闻可确认公司收入/订单。 | B1（公司经营）+B2（产品） | 合并收入无法拆给 Cu–Cu；未公开特定AI/HBM客户或键合产品产出。 | 对 D2W、RDL 和薄晶圆 handling 的组合价值高，仍须客户验证。 |
| | **ASMPT** | 年报可确认半导体解决方案与 SMT 的合并经营；其组合包括 die bonding、molding、assembly、inspection。 | B1 + B2 | 不能把总收入或 die-bonding产品线写成 direct Cu–Cu market share。 | 对封装后段自动化/组装重要；direct bonding是否采用取决于具体平台。 |
| **临时键合/解键合** | EVG、SUSS、Brewer Science材料体系等 | EVG/SUSS公开 temporary bonding/debonding 解决方案。 | B2 | 未披露客户使用在 8层或 HBM 的比例。 | 临时载体、胶材、解键合温度/激光/机械应力和残胶是超薄晶圆良率门槛。 |
| **减薄、磨削、切割/划片** | **DISCO**、TOKYO SEIMITSU/ACCRETECH、ADT等 | DISCO财报可确认其 grinding/saw/dicing设备实际销售。 | B1（公司业务收入）+B2（产品） | 未按 HBM、CIS、3D IC和具体客户拆分；没有每台设备对应 stack 数的换算。 | 多层堆叠中 TTV、翘曲、边缘破损、背面金属暴露和薄晶圆搬运直接决定后段良率。 |
| | **EVG/SUSS** | 结合临时键合/解键合与薄晶圆处理平台。 | B2 | 同上。 | W2W/D2W 之后的减薄流程可决定背面加工是否可行。 |

### 3.3 量测、检查、测试、可靠性、自动化和厂务

| 环节 | 全球厂商 | 事实状态 | 核心瓶颈 | “实际产能”应看什么 |
|---|---|---|---|---|
| **overlay/CD/膜厚/缺陷/键合后检查** | KLA、Onto Innovation、Camtek、Nova、EVG/ SUSS相关计量 | KLA FY2025财报可确认公司收入；各厂商有先进封装/过程控制产品。属于 B1+B2，而非键合产品量。 | buried void、颗粒、Cu pad/介质缺陷、overlay、薄晶圆 TTV、表面形貌；direct bonding 的许多缺陷需要在不可返工前发现。 | 工具验收、缺陷检出率/漏检率、客户的 defect density、良率相关性；这些通常不公开。 |
| **电性/高速测试、KGD、burn-in** | Advantest、Teradyne、Cohu、Chroma、OSAT内部测试 | Advantest FY2024财报确认测试系统收入/订单；其他测试商年报亦可确认自身业务。 | KGD、TSV continuity、宽I/O、BER、热、burn-in和系统级测试。 | 测试秒数、并测数、yield、stack test coverage、BER/热循环；不是 tester 收入。 |
| **自动化/搬运/MES/追溯** | Brooks Automation/Azenta、Rorze、Hirata、Daifuku、设备厂内建EFEM等 | 自动化商有设备产品和公司收入，但极少按 hybrid-bond拆分。 | 薄晶圆/临时载体搬运、queue time、颗粒、批次追溯、recipe管理。 | OEE、particle excursion、carrier breakage、WIP/queue time和批次良率。 |
| **厂务与超纯化学品/气体/UPW** | Entegris、Air Liquide、Linde、Merck等 | 为半导体厂提供材料/气体/过滤/化学品是公开业务事实。 | Cu/离子污染、UPW质量、化学品过滤、洁净室颗粒、热预算和废液处理。 | 关键指标是现场 specification、supply continuity、qualification，不能以厂务公司营收推键合产量。 |

---

## 4. 中国全链条对照：模块参与者、真实能力与披露缺口

### 4.1 直接键合与三维集成设备：最接近核心工艺但仍需区分验证和量产

| 工艺模块 | 中国参与者 | 已取得的公开事实 | 标签 | 客户/产能/路线图边界 |
|---|---|---|---|---|
| **W2W/C2W键合与预处理** | **拓荆科技（Piotech）** | 公司公开互动曾称研制晶圆对晶圆混合键合产品和芯片对晶圆键合表面预处理产品；其后公司/媒体披露 Dione 300 已通过客户验证并实现产业化应用的线索。 | B2；无原互动永久链接的媒体转述降为B5 | 公开资料不披露客户名称、工具台数、用于 Cu–Cu还是其他键合、实际利用率、良率或 die产出。不能把“产业化应用”写成八层AI memory量产。 |
| **CMP/平坦化、减薄** | **华海清科** | 官网称 12英寸 Universal CMP 可实现晶圆纳米级全局平坦化，部分型号已在集成电路/先进封装批量应用；其 Versatile GP/GH 系列面向 3D IC和先进封装超精密减薄，集成磨削、CMP、清洗与TTV/缺陷控制。 | B2 | “先进封装批量应用”没有拆分为 Cu–Cu hybrid bond；无客户、Cu recess、roughness、键合良率、工具数或具体产品披露。官网再生晶圆月产能也不能用于推 hybrid-bond有效产能。 |
| **清洗、湿法、电镀** | **盛美上海（ACM Research Shanghai）** | 公司公开单片清洗、湿法、电镀和先进封装产品平台；定期报告可确认公司总收入。 | B1+B2 | 无公开A1/A2显示具体直键合设备型号、客户、颗粒/金属污染指标、客户验收或与八层结构关联。 |
| **TSV刻蚀/薄膜/清洗** | **北方华创、中微公司、拓荆** | 北方华创有刻蚀、PVD/CVD/ALD与清洗；中微有等离子体刻蚀/MOCVD；拓荆有 PECVD/SACVD/ALD及三维集成布局。上市公司年报能确认合并收入。 | B1+B2 | 不披露用于何种TSV、memory、direct bonding或客户；不能从收入/腔体数推 TSV wafer 或 stack。 |
| **量测/缺陷检查** | **中科飞测、精测电子** | 两公司公开前道/封装量测、缺陷检测、膜厚/CD/overlay等产品并有经营披露。 | B1+B2 | 未披露 Cu–Cu 键合空洞、界面/overlay、薄化 TTV 的客户验收、检出率或 A4E/任何命名项目。 |
| **材料** | **安集科技、鼎龙股份**及湿电子/电镀/封装材料生态 | 年报/产品资料可确认 CMP slurry、抛光垫、功能湿电子化学品等业务。 | B1+B2 | 没有混合键合专用牌号、客户资格、批次、界面可靠性、供应比例或与算苗关系。 |
| **测试** | **长川科技、华峰测控**及封测厂自有测试 | 测试设备企业有产品线与合并经营披露。 | B1+B2 | 无公开八层stack的 KGD、BER、burn-in、测试秒数、良率或客户验收。 |

### 4.2 中国制造/封测与下游：3D能力、研发与稳定量产不可混写

| 参与者 | 可确认的公开位置 | 标签 | 应有而未披露的字段 | 正确写法 |
|---|---|---|---|---|
| **中芯国际/华虹等晶圆厂** | 有逻辑晶圆制造、特殊工艺和先进封装相关生态位置；公司年报披露总营收/CapEx。 | B1/B2 | 确切 W2W/D2W Cu–Cu 工艺、memory/logic产品、客户、良率、每月有效产能。 | 可写“潜在制造环节”；不写“为某AI 3D芯片代工/键合”。 |
| **盛合晶微、长电科技、通富微电、华天科技等** | 先进封装、TSV/2.5D/3D和测试为各家公开战略/技术方向；华天在互动中称开展混合键合封装技术研发。 | 合并收入 B1；产品/研发 B2；无原始文件的媒体为B5 | 具体 Cu–Cu产品、客户、量产、稳定良率、产能、测试覆盖。 | “布局/研发/平台”不能换成“已获得 HBM/AI客户”或“八层量产”。 |
| **国内EDA：华大九天、概伦电子、芯和等** | 提供模拟、DFM、封装/电源/可靠性或工艺建模工具。 | B1/B2 | 3D PDK、direct-bond规则、sign-off案例、具体客户流片。 | 可写“设计流候选”，不能写“已完成某Cu–Cu签核”。 |
| **算苗科技等下游设计方** | 官网自述3D TokenPU/混合键合叙事，媒体称A4E流片与8层存储—logic堆叠。 | 官网B2、媒体B5 | Cu–Cu方式、供应商、容量BOM、良率、出货、收入。 | 不能把所有国内工艺相关公司自动并入其供应链。 |

**中国链的真正结论：** 国内已存在直键合装备、CMP/减薄、清洗/电镀、刻蚀/沉积、量测、测试、材料和先进封装的多模块参与者。其中拓荆的 W2W/C2W 公共产品线、华海清科的平坦化/减薄和盛美的清洗/电镀最贴近 Cu–Cu 工艺要求。但公开资料仍没有形成“指定 3D 产品—完整中国设备材料BOM—工艺验收—稳定良率—实际出货”的闭环。投资或产业判断应把这称为**国产化能力建设与客户认证机会**，而不是既成规模供货。

---

## 5. 路线图：Cu–Cu、TSV+bump、HBM及多层堆叠各自走向何处

### 5.1 三条工艺路线并行，而非单一替代

| 路线 | 当前最适用位置 | 优势 | 主要限制 | 与 HBM 的关系 |
|---|---|---|---|---|
| **TSV + micro-bump/TCB** | HBM堆叠、2.5D逻辑+HBM、成熟 chiplet 封装 | 产业经验、可返工/测试策略相对成熟、供应链广 | bump pitch、热、翘曲、堆高、功耗和互连密度 | 仍是大量 HBM/2.5D 产品的重要路线；HBM代际升级并不自动淘汰它。 |
| **Cu–Cu/介质 hybrid bonding** | 逻辑—缓存、CIS、部分高密度 3D logic、极细 pitch异构集成；未来可能扩展到更多存储/逻辑组合 | 极细互连、短路径、降低互连寄生、潜在带宽/能效优势 | 平坦度/颗粒/污染/overlay/可靠性、不可返工、测试和成本 | 可与HBM系统共同出现；**HBM4不等于全面采用 hybrid bonding**。必须逐厂商、逐产品确认。 |
| **RDL/中介层/扇出/玻璃基板等横向互连** | 多chiplet、超大封装、AI加速器和网络/光电集成 | 系统级可扩展性、异构集成灵活 | RDL层数、翘曲、基板、热、电源、面积与成本 | 与HBM package强相关，但不是memory die vertical bonding的同义词。 |

### 5.2 多层（例如“8层 memory + logic”）的转折点不在堆层数，而在有效良率

八层是复杂度提示而非产能指标。每一层都可能引入 memory wafer/die KGD、TSV/背面、薄化、键合、对准、热应力和测试失效。最终有效良率不是由任何一家键合机供应商的交期决定，而是由以下乘积式因素决定：

```text
有效成品率 ≈ 各层合格晶圆/裸片率 × 各次键合通过率 × TSV/背面加工通过率
             × 键合后检查通过率 × 封装/热/电性测试通过率
```

上式只解释为什么多层复杂度急剧上升，**不是本报告对任何产品的数值模型**。没有逐层良率、键合次数、die数和测试覆盖数据，不能从“8层”“流片”或设备订单估算可交付产品数。

多层路线的实际转折点和跟踪指标如下：

| 关键门槛 | 必须看到的证据 | 不能用什么替代 |
|---|---|---|
| 键合前平坦度与表面准备 | Cu recess/roughness、颗粒、金属污染、清洗后表面与队列时间 | CMP机出货、材料商收入、论文样品 |
| W2W/D2W 选择 | 结构截面、对准/pitch、die尺寸、临时键合与背面流程 | 新闻中笼统的“3D堆叠” |
| 键合质量 | void、overlay、键合强度、界面电阻、退火窗口、可靠性 | 设备名、产线开工、样品照片 |
| KGD和测试 | 每层测试、TSV continuity、burn-in、BER、系统工作负载 | tester订单或封测厂合并收入 |
| 热/PDN | hotspot、热阻、IR drop、EM/TDDB、热循环/湿热 | 单一峰值带宽/理论性能 |
| 商业化 | 客户验收、收入确认、实际交付单位或可复核量产声明 | 融资、招聘、tape-out、概念股报道 |

---

## 6. 实际订单、交付、产能与扩产：可写的事实账本

| 公司/环节 | 可确认的实际发生 | 标签 | 正确的产业含义 | 不可做的换算 |
|---|---|---|---|---|
| Besi | FY2025收入 €591.3m、全年订单 €685.0m、Q4订单 €250.4m。 | B1 | 先进封装/2.5D/光子和hybrid-bond相关设备需求是订单解释的一部分。 | 订单 ÷ 单价 ≠ 客户工具数；工具数 ≠ bonded die/HBM stack。 |
| Applied/Lam/TEL | 正式财报确认其各自的总营收、分部收入/订单和资本设备业务。 | B1 | 前道设备周期确有真实商业活动，影响TSV、存储、封装相关能力建设。 | 合并或分部营收 ≠ 3D IC/混合键合收入或产能。 |
| DISCO | 财报确认磨削/切割设备业务收入。 | B1 | 超薄晶圆处理是3D堆叠的必要工序。 | DISCO销售 ≠ 薄化合格晶圆、HBM stack或键合成功率。 |
| Advantest | FY2024财报确认测试系统收入/订单。 | B1 | 测试资本开支是AI/HPC/存储产品复杂度上升的旁证。 | tester收入 ≠ KGD、BER或实际芯片出货。 |
| 拓荆 | W2W/C2W混合键合设备/表面预处理的公司声明及客户验证/产业化线索。 | B2/B5 | 中国直键合装备已进入客户验证/产业化观察阶段。 | 无客户与产量时，不能称“国产直键合有效产能”或某项目供货。 |
| 华海清科 | CMP、减薄和先进封装产品公开称在相关制造工艺批量应用。 | B2 | 说明国内平坦化/薄化模块已有商业应用基础。 | 不等于 Cu–Cu direct-bond客户端/良率/产能。 |
| 盛美/北方/中微/中科飞测/精测等 | 公司年报收入与产品模块。 | B1/B2 | 形成国内工艺模块供给池。 | 不得拼接为单一客户的“全国产键合产线”。 |

对扩产和爬坡，正确的时间描述是：设备制造/交付通常以月到季度计；洁净室安装、工艺 recipe、材料匹配、计量闭环和客户 qualification 通常为多季度；稳定良率和成本下降可能跨 1—2 个产品周期。这是 **B6 行业经验区间**，不是任何公司承诺。新闻中的厂房开工、CapEx、设备下单和客户送样都只能进入 B3/B5 前瞻表，绝不能计为当期实际 hybrid-bond有效产能。

---

## 7. 至少20个一手来源：链接、日期、可使用的范围

下表仅列公司IR、公司产品/技术页或官方组织资料。页面没有发布日期时写明“访问日”；它们证明的是所写范围，不自动证明下游客户、实际封装量或供应关系。

| # | 一手来源 | 日期 | 可用于确认的内容 |
|---:|---|---|---|
| 1 | Besi FY2025 results：https://www.besi.com/investor-relations/press-releases/details/be-semiconductor-industries-nv-announces-q4-25-and-full-year-2025-results/ | 2026-02-19 | Besi收入、订单及公司对先进封装/hybrid-bond需求的表述。 |
| 2 | EV Group官网：https://www.evgroup.com/ | 访问2026-07-28 | bonding、alignment、temporary bonding/debonding、metrology产品能力。 |
| 3 | SUSS IR新闻：https://www.suss.com/en/investor-relations/news/ | 访问2026-07-28 | 公司业绩和先进封装设备平台。 |
| 4 | ASMPT financial reports：https://www.asmpt.com/investor-relations/financial-reports/ | 访问2026-07-28 | 半导体解决方案合并经营与产品组合。 |
| 5 | Applied FY2024 results：https://ir.appliedmaterials.com/news-releases/news-release-details/applied-materials-announces-fourth-quarter-and-fiscal-year-2024-results | 2024-11-14 | 公司/分部收入，不拆为3D IC。 |
| 6 | Lam FY2025 results：https://newsroom.lamresearch.com/2025-07-30-Lam-Research-Corporation-Reports-Financial-Results-for-the-Quarter-Ended-June-29,-2025 | 2025-07-30 | 公司收入与系统销售。 |
| 7 | TEL earnings library：https://www.tel.com/ir/library/earnings/ | 访问2026-07-28 | TEL订单/销售等财务披露。 |
| 8 | DISCO financial information：https://www.disco.co.jp/eg/ir/financial_information/ | 访问2026-07-28 | 磨削、切割相关设备业务财务。 |
| 9 | KLA FY2025 results：https://ir.kla.com/news-releases/news-release-details/kla-corporation-announces-fourth-quarter-and-fiscal-year-2025-results | 2025-07-31 | 公司过程控制业务收入。 |
| 10 | Advantest FY2024 results：https://investor.advantest.com/en/ir/news/2025/20250425.html | 2025-04-25 | 测试系统业务财务。 |
| 11 | Teradyne SEC filings：https://investors.teradyne.com/financial-information/sec-filings | 访问2026-07-28 | 自动测试业务的年报/季报。 |
| 12 | Entegris annual reports：https://investor.entegris.com/financial-information/annual-reports | 访问2026-07-28 | 材料/过滤/化学品相关经营披露。 |
| 13 | Fujimi IR：https://www.fujimico.com/eng/ir/ | 访问2026-07-28 | CMP slurry等材料业务公司披露。 |
| 14 | Ajinomoto ABF：https://www.aft-website.com/en/products/abf/ | 访问2026-07-28 | ABF材料产品事实。 |
| 15 | 拓荆科技IR：https://www.piotech.cn/ir/ | 访问2026-07-28 | 定期报告、三维集成/薄膜设备公司披露。 |
| 16 | 华海清科官网：https://www.hwatsing.com/ | 访问2026-07-28 | CMP、减薄、清洗和先进封装/3D IC产品能力。 |
| 17 | 盛美上海IR：https://www.acmrcsh.com/investor-relations/ | 访问2026-07-28 | 清洗、电镀、湿法及公司财务披露。 |
| 18 | 北方华创财务报告：https://www.naura.com/EN/IR/FinancialReports/ | 访问2026-07-28 | 公司收入及刻蚀/薄膜/清洗布局。 |
| 19 | 中微公司报告：https://www.amec-inc.com/en/ir/reports.html | 访问2026-07-28 | 公司收入及等离子体刻蚀产品布局。 |
| 20 | 中科飞测官网：https://www.zkftech.com/ | 访问2026-07-28 | 量测/缺陷检测产品范围。 |
| 21 | 精测电子IR：https://www.wuhanjingce.com/ | 访问2026-07-28 | 半导体量测/检测与经营披露。 |
| 22 | 安集科技IR：https://www.anjimicro.com/ | 访问2026-07-28 | CMP slurry/功能湿电子化学品相关业务。 |
| 23 | 鼎龙股份IR：https://www.dinglong.cn/ | 访问2026-07-28 | CMP抛光垫/材料相关业务。 |
| 24 | 长电科技IR：https://www.jcetglobal.com/investor/ | 访问2026-07-28 | 先进封装测试公司披露。 |
| 25 | 通富微电IR：http://www.tfme.com/ | 访问2026-07-28 | 封测公司经营和先进封装布局。 |
| 26 | 华天科技IR：https://www.ht-tech.com/ | 访问2026-07-28 | 封测企业定期报告/技术布局（网站访问受限时须回查交易所文件）。 |
| 27 | Synopsys 3DIC Compiler：https://www.synopsys.com/implementation-and-signoff/3dic-compiler.html | 访问2026-07-28 | 3D IC设计/签核工具存在。 |
| 28 | Cadence Integrity 3D-IC：https://www.cadence.com/en_US/home/tools/ic-package-design-and-analysis/integrity-3d-ic-platform.html | 访问2026-07-28 | 3D封装协同设计工具存在。 |
| 29 | Siemens EDA：https://eda.sw.siemens.com/ | 访问2026-07-28 | Calibre/3D IC相关EDA能力。 |
| 30 | IEEE Heterogeneous Integration Roadmap：https://eps.ieee.org/technology/heterogeneous-integration-roadmap.html | 访问2026-07-28 | 异构集成技术与供应链参考框架。 |

---

## 8. B组最终判断：谁强、什么卡、怎样避免研究误判

1. **最稀缺的不是“混合键合概念”，而是工艺闭环。** 全球设备端 Besi、EVG、SUSS、ASMPT 和前道/计量/测试厂商覆盖关键模块；中国端拓荆、华海清科、盛美、北方华创、中微、中科飞测、精测及材料/OSAT 形成模块生态。胜负由 CMP—清洗—对准—键合—薄化—检测—KGD/可靠性是否闭环决定。
2. **Besi 的订单/收入是本组最清晰的先进封装设备商业证据之一，但仍只是设备侧 B1。** 它可以支持“需求在增强”，不能支持“某产品已出货多少层/多少die”。
3. **中国直接键合关键设备值得跟踪，但披露颗粒度还不足以量化竞争份额。** 拓荆 W2W/C2W、华海清科 CMP/减薄、盛美清洗/电镀是最接近的公开能力节点；但无完整客户、良率、产量和收入闭环时，只能给“客户验证/模块参与”评价。
4. **HBM、TSV+bump和Cu–Cu hybrid bonding会长期并行。** HBM提升的主要是高带宽DRAM系统能力；hybrid bonding是超细垂直互连工艺。二者有CMP、清洗、薄化、检测、测试、热/EDA交集，却不能互相替代，更不可把 HBM4 自动写成 Cu–Cu全面量产。
5. **下一轮尽调最值得索取的字段**是：键合方式（W2W/D2W、Cu–Cu/介质/TCB）、pitch、Cu recess/颗粒/overlay、工具型号与验收、每层KGD、每次键合与最终yield、可靠性、BER/功耗/有效带宽、客户验收、可交付单位。这些比“扩产金额”“设备订单”和“团队量产经验”更能决定商业价值。

