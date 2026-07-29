# 第4研究组：2026–2031全球3D IC竞争、路线图、客户起量与利润池

**研究截点：2026-07-29｜组别：run_d｜证据口径：产品级闭环优先**
**本轮在线状态：** 按用户要求仅尝试 Codex 内置浏览器，运行环境返回 `Browser is not available: iab`；未改用桌面 Chrome。本文因此以仓库内此前由主任务核验的一手来源台账、公司网页摘录和法定披露为底稿。本轮未能重新打开网页的项目均标为“待主控复核”，不升级为实时事实。

## 0. 先把四个市场拆开

|口径|本文定义|已发生的商业事实|绝不能混入的量|
|---|---|---|---|
|**3D IC**|至少两个有源/功能 die 或 wafer 在垂直方向形成电连接的集成；可包含 TSV+micro-bump/TCB 或 direct bonding|stacked CIS、部分3D NAND分离阵列/外围、AMD 3D V-Cache、一般Foveros等|纯2.5D横向chiplet、单片先进节点收入|
|**Hybrid Bonding（HB）**|介质直接键合与嵌入导体（通常Cu）互连结合的无焊料细间距工艺；需逐产品确认|Sony部分堆叠CIS技术、TSMC SoIC/AMD 3D V-Cache生态是强例证；3D NAND须逐代核验|所有“stacked”“direct bonded”“CuA”“Foveros”“X-Cube”的总出货|
|**HBM**|JEDEC高带宽DRAM产品、接口和stack体系；通常含TSV，量产主流长期使用TCB/micro-bump|三大DRAM厂的HBM3E/HBM4产品、客户样品、收入属于HBM市场|不得把HBM收入/stack数直接计成HB收入；HBM4不等于HB|
|**2.5D**|逻辑、HBM等die通过interposer/RDL/bridge横向集成|CoWoS、EMIB、I-Cube/H-Cube等已经大规模服务AI/HPC|不得把CoWoS名义产能、GPU销量、2.5D封装收入计为3D direct-bond数量|

这一区分决定竞争结论：2026–2031最大的**系统价值池**可能仍由HBM+2.5D承载，而最快增长的**工艺增量**可能来自D2W混合键合、KGD/检测/测试和3D设计；两者相关，却不是同一收入池。

## 1. 结论先行

1. **TSMC拥有最强的“先进逻辑节点—SoIC—CoWoS—客户生态”组合优势。** SoIC支持W2W/D2W、从sub-10µm规则起步，官网称3nm stacking technology于2025进入volume production；这是平台/工艺量产状态，不是SoIC有效WPM、客户die数量或收入。AMD 3D V-Cache证明产品闭环，但AMD未拆SKU销量。
2. **Intel是全栈挑战者，但一般Foveros与Foveros Direct必须分开。** Lakefield/Meteor Lake等只能证明Foveros产品商业化；Foveros Direct的真正拐点是首个具名、可售、客户确认且重复量产的direct-bond SKU，而不是技术页或工厂投产。
3. **Samsung的潜在优势是foundry、HBM、CIS、封装同集团协同，现实短板是产品级透明度。** X-Cube是公开3D平台，I/H-Cube是2.5D系统封装；二者及Samsung HBM收入均不能证明特定Cu–Cu产品起量。
4. **Sony在CIS direct bonding的商业学习曲线领先；YMTC/Kioxia在array–periphery分离键合NAND上已有产品路线。** 它们分别服务影像和cost/bit，不应套用AI逻辑3D的ASP、良率或客户节奏。
5. **HBM在2026–2031是最大邻接需求池，却未必是混合键合最早的增量来源。** TCB/micro-bump仍有改进空间；16-high、HBM4E或后续代际可能提高HB的经济动机，但必须等DRAM厂+客户的产品/工艺联合证据。
6. **利润最厚的不一定是键合设备。** 真正稀缺的组合是：3D PDK/IP和架构共优化、KGD与高覆盖测试、CMP/清洗/overlay/void闭环、热/PDN/机械签核、合格量产产能和客户资格。单机订单容易被周期放大，量产数据库和客户切换成本更持久。
7. **2026–2031的竞争格局更可能“分赛道寡头+局部第二来源”，而非一家通吃。** CIS由垂直IDM强势；NAND由存储IDM控制；高端logic 3D由leading foundry/IDM掌握；OSAT在区域化、测试、末端集成和中端D2W服务中扩张。

## 2. 主要玩家：平台、产品、客户与下一代转折点

|玩家|3D/HB产品或技术|截至截点可证商业状态|主要客户需求/起量方式|2026–2031下一代转折点|可用/不可用边界|
|---|---|---|---|---|---|
|**TSMC**|SoIC-X/3DFabric；W2W/D2W；与CoWoS/SoW/COUPE生态协同|官网称3nm stacking于2025 volume production；AMD 3D V-Cache为产品生态实证|HPC/CPU/AI客户要求高带宽、低功耗、异节点复用、PDK/签核和稳定交付；从联合设计到工程批、qualification、量产|多客户3nm/N2产品闭环；D2W KGD、热/PDN和良率跨产品复制；SoIC与2.5D/光子组合|可确认平台/工艺状态；**不可**用TSMC总收入、先进封装CapEx、CoWoS WPM换算SoIC量|
|**AMD**|3D V-Cache，SRAM-on-logic|Ryzen/EPYC多代可售产品，证明不是一次试产|游戏/HPC/server客户购买更大缓存、低延迟和能效；SKU由性能溢价与软件适配起量|从更多CPU SKU向更广cache/logic组合扩展；是否进入更多AI产品需逐SKU确认|可写产品上市；**不可**从AMD CPU收入反推3D cache die、SoIC收入或键合良率|
|**Intel**|Foveros；Foveros Direct；EMIB|一般Foveros有Lakefield/Meteor Lake等商业产品；Direct量产SKU闭环未取得|内部产品先学习；外部foundry客户要求PDK、IP安全、交付和second source|首个明确标注Foveros Direct的可售量产产品；外部客户design win；Direct+EMIB组合的重复交付|一般Foveros出货不能计Direct/HB；foundry总收入不能分拆|
|**Samsung Foundry/DS**|X-Cube 3D；I/H-Cube 2.5D；ISOCELL；HBM|平台与商业产品族存在；未取得具名X-Cube Cu–Cu客户量产闭环|逻辑、存储、CIS客户分别重视性能、供给、可靠性；集团协同只有在共同qualification后才兑现|X-Cube W2W/D2W/Cu界面的客户SKU；先进逻辑+HBM+封装共同设计赢|平台页和DS收入仅证能力；**不可**把HBM、CIS或I/H-Cube总量算成HB|
|**Sony Semiconductor Solutions**|Exmor RS、stacked CMOS、two-layer transistor pixel、Cu–Cu connection技术|堆叠CIS长期商用，是高volume direct-bond重要例证|手机、相机、汽车客户要求图像质量、低噪、高动态、global shutter、长期可靠性|更多逻辑功能/堆叠、车载/工业资格；转折点是良率和OEM采用而非最小pitch|可确认产品/技术路线；不可把Sony所有sensor或手机出货全算Cu–Cu|
|**YMTC**|Xtacking，array wafer和periphery wafer分离制造/键合|多代产品路线商业化|SSD/终端客户核心是cost/bit、性能、固件、耐久和供给|更高层数下键合良率/成本优势；企业SSD认证；设备材料连续性|可确认分离制造+wafer bonding；Cu–Cu机制和各代出货需逐代核验|
|**Kioxia/Western Digital生态**|CBA（CMOS directly Bonded to Array）、BiCS FLASH|CBA为公司公开商业路线|NAND客户按cost/bit、性能、耐久、控制器生态起量|BiCS新代际的CBA重复量产与企业SSD采用|`directly bonded`不自动证明Cu/oxide HB细节；不拆CBA收入|
|**SK hynix**|HBM3E/HBM4路线；4D NAND|HBM/NAND商业化；HBM增长为实际存储需求，不代表HB|AI accelerator客户采用前需性能、功耗、热、良率、长期供货认证；通常提前多个季度送样/锁量|HBM4/4E、12/16-high及logic base die的客户资格；若原厂宣布HB才构成HB窗口|可用财报/产品公告确认HBM业务；不可转换成hybrid-bond stack数|
|**Micron**|HBM3E/HBM4；3D NAND CuA|2025公司公告称向关键客户送36GB、12-high、>2TB/s HBM4样品；这是样品不是销售量|AI客户送样→qualification→供应分配→收入；NAND与HBM周期分开|HBM4客户量产资格、HBM4E/16-high；是否采用HB必须逐产品证实|CuA是CMOS-under-array，不是Cu–Cu；样品不等于量产|
|**ASE**|VIPack及先进封装/2.5D/测试；相邻D2W能力|先进封装商业存在；未获统一HB有效产能/收入|客户需要多厂区域交付、KGD、测试、热、可靠性和末端组装|取得具名D2W/HB产品资格及复购；与foundry前道协作|OSAT总先进封装收入、厂房投资不能计HB|
|**Amkor**|SWIFT/SLIM、2.5D/3D、测试；美国区域化项目|先进封装商业化；具体HB产品量需另证|美国AI/汽车/国防客户重视在岸供应、IP和长期可靠性|Arizona等新产能从建设→装机→qualification→客户收入；HB须逐产品证明|项目金额/开工不是可用HB产能|
|**JCET/长电科技**|XDFOI/先进封装、测试及区域服务|公司先进封装业务可证；无统一可审计HB出货|中国/全球客户需要成本、交期、测试覆盖、供应安全|D2W/HB共同开发、客户验证、持续季度收入；国产设备材料导入|总收入、XDFOI或2.5D产品不自动计HB|
|**Besi / EVG / SUSS / ASMPT**|D2W placement、W2W/HB、临时键合/解键合、先进封装工具|产品线和设备周期可证；客户产品量不可由订单推出|制造客户先DOE/验收，再工艺qualification、扩线、复购|多客户复购、产能利用率、服务收入、从研发机到量产cluster复制|订单/设备收入是领先指标，不是wafer/die实际产量|
|**Xperi/Adeia**|DBI direct-bond互连IP/许可|IP/技术存在；客户和产品采用需逐项披露|客户购买FTO、工艺缩短开发周期和生态兼容|许可续约、更多foundry/IDM产品采用、诉讼/FTO清晰度|专利覆盖不等于产品采用或出货|
|**Synopsys/Cadence/Siemens**|3DIC Compiler、Integrity 3D-IC、Calibre等|工具平台存在|客户要求芯片—封装协同、热/应力/PDN/SI/DFT和sign-off|PDK认证、HB接口模型、跨foundry可移植与量产tape-out数量|软件总收入不等于3D IC收入；tape-out不等于量产|

## 3. 客户需求与起量节奏

### 3.1 不同客户的购买逻辑

|客户群|真正购买的价值|先决条件|典型起量形态|最易误判的信号|
|---|---|---|---|---|
|手机/CIS OEM|图像质量、像素/逻辑分离、面积、高速读出|sensor良率、模组/镜头协同、终端影像算法与可靠性|一个旗舰型号design win后按手机周期爬坡，再向更多型号扩散|技术发布、样片或传感器总出货|
|NAND/SSD客户|cost/bit、性能、容量、耐久与固件|多层良率、控制器/firmware、企业级qualification|消费产品先规模、enterprise认证更慢；强周期性|NAND层数、IDM总bit shipment|
|CPU/HPC客户|cache容量、latency、能效、TCO|高价值KGD、热/PDN、软件、可靠性、平台供货|少数高ASP SKU先起量，成功后代际延续|benchmark、tape-out或平台可用|
|AI accelerator/CSP|带宽/功耗/封装面积、部署TCO、稳定供给|HBM+logic+2.5D/3D共同资格、散热、板级和集群验证|样品→工程系统→小批部署→多季度放量；客户高度集中|CoWoS扩产、HBM预订或设备订单被当作HB销量|
|汽车/工业|寿命、失效率、温度范围、追溯与长期供货|AEC/ISO等系统级资格、工艺冻结、second source|验证期长、斜率慢，design win生命周期长|“车规级能力”或实验室可靠性结果|
|CPO/网络客户|I/O带宽密度、功耗、交换机TCO|光源、热、可维修性、封装良率和网络生态|先在最高端交换/专用集群小量，再看标准化|器件演示、合作MOU、单条链路性能|

### 3.2 从技术到销量的七级漏斗

1. 技术论文/专利/平台发布；
2. 设备安装、工艺DOE、test vehicle；
3. 可工作的样片和初始良率；
4. 工艺qualification与可靠性；
5. 客户产品qualification、系统验证；
6. 具名可售SKU、稳定季度交付；
7. 多客户/多产品复制、扩产和复购。

只有第6–7级可称“起量”。第1–5级只适合作为领先指标。直接键合不可返修、缺陷会随层数放大，故D2W的KGD和pre-bond coverage决定客户是否敢从第4级进入第5级。

## 4. 2026–2031逐年竞争事件与领先指标

> 下表不是厂商销量承诺。2026列含已发生/可验证状态；2027–2031均为本组A6条件情景和应观察的证伪指标。用户所谓“未来五年”以2026为基准、2031为五年终点，共列六个自然年。

|年份|基准情景的产业事件|主要玩家/客户动作|最重要领先指标|若未出现意味着什么|
|---:|---|---|---|---|
|**2026**|CIS/NAND维持商业规模；AMD V-Cache/SoIC继续作为logic-on-cache锚；AI系统仍主要靠HBM+2.5D；HBM4进入送样/资格和初始产品周期|TSMC推进3nm SoIC平台量产学习；三大DRAM厂竞争HBM4资格；OSAT/设备商扩充先进封装能力|具名SKU的工艺映射；客户qualification措辞；设备复购而非首台；KGD/热/可靠性数据|若只有CapEx/平台新闻，说明“产能故事”尚未转成可用产出|
|**2027**|精选logic/cache和近存3D进入新一轮工程/初始收入；HBM4系统放量但HB采用仍逐产品|TSMC多客户SoIC设计赢；Intel寻求Foveros Direct产品闭环；Samsung寻求X-Cube具名客户；CSP验证近存/3D AI|客户联合公告、可售SKU、季度收入贡献、量产良率趋势；HBM厂明确stack bonding工艺|没有产品闭环则Direct逻辑3D扩张晚于设备周期，TCB/2.5D继续占主导|
|**2028**|D2W由cache向部分logic-on-logic/AI chiplet扩展的首个关键窗口；CPO仍以高价值小量为主|leading foundry和至少一家IDM/OSAT争取第二来源；EDA/PDK/DFT流程趋于标准化|第二/第三客户、重复订单、多产品复制；post-bond defect/yield、热和测试成本下降|若仍停留单客户单产品，产业是高价值利基而非广泛平台|
|**2029**|若前两年资格通过，direct-bond容量利用率和服务收入开始显著；HBM4E/更高层stack提高HB评估动力|DRAM厂决定TCB继续缩pitch还是在部分stack切HB；CPO可能出现第一批可审计系统部署|原厂量产公告+客户产品映射；HB设备复购与终端收入同步；16-high热/高度/可靠性数据|若TCB满足要求，HBM邻接需求增长但HB增量后移；设备利用率风险上升|
|**2030**|3D logic由“是否可做”转向“在哪些架构有ROI”；区域化OSAT承接更多中后段服务|CSP定制ASIC、CPU/AI厂将3D cache/logic作为部分平台选项；多地域供应链资格|多代产品延续、second source、标准接口/PDK、客户切换成本；每系统TCO改善|若没有代际延续，首代产品可能是一次性工程项目，利润池回到foundry/2.5D|
|**2031**|基准情景形成分赛道常态：CIS/NAND成熟，logic/cache选择性普及，CPO/后续memory-on-logic高价值渗透，TCB/2.5D长期并存|TSMC仍可能占高端生态优势；Intel/Samsung/OSAT能否缩小差距取决于外部客户；设备/IP/EDA从单机/许可转为经常性服务|3家以上制造平台的可售HB SKU、多客户稳定季度收入、按工艺拆分披露或可信容量利用率|若仍无拆分披露，应降低2031市场额置信度，不能用先进封装总额补洞|

### 4.1 三个真正的转折点

- **产品转折：** 不是pitch更小，而是首个/第二个客户可售SKU进入连续季度交付。
- **经济转折：** 不是键合yield单点提高，而是“每层KGD × 各次键合yield × 最终测试yield × 可售ASP”的完整堆叠经济性胜过2.5D/TCB。
- **产业转折：** 不是一家leading foundry成功，而是另一制造平台/OSAT获得外部客户qualification，形成可替代供给。

## 5. 商业模式与利润池

|利润池|收费模式|为什么可能高毛利|谁更有优势|2026–2031商业机会|主要风险|
|---|---|---|---|---|---|
|3D架构/EDA/PDK/IP|工具订阅、IP许可、NRE、sign-off服务|进入设计早期、切换成本高、可跨多产品复用|foundry自有PDK、Synopsys/Cadence/Siemens、Adeia/Xperi|热/应力/PDN/DFT、HB接口模型、FTO、本土EDA|客户集中、IP诉讼、工具总收入难拆分|
|leading foundry 3D制造|wafer制造+3D集成+先进封装服务、NRE|控制先进节点、良率数据库和客户生态|TSMC；Intel/Samsung挑战|SoIC/D2W、logic-on-cache/logic、3D+2.5D组合|高CapEx、不可返修、客户集中、产能错配|
|OSAT集成/区域化|package/test单价、联合开发、长期供货|客户需要second source、在岸供应、测试和末端集成|ASE、Amkor、JCET等|D2W、KGD、热、可靠性、区域新厂|被foundry内部化；技术项目不一定转量产|
|键合/前处理设备|设备销售、升级、服务、备件|关键工具验证周期长，量产线复购可形成黏性|Besi、EVG、SUSS、ASMPT及前处理设备厂|从首台验证到cluster复制；W2W/D2W并行|订单先于终端需求，周期和客户集中度高|
|CMP/清洗/沉积/材料|设备、slurry/pad/化学品按耗用量；联合recipe|耗材经常性收入；表面微小偏差直接决定良率|Applied/Lam/TEL/SCREEN/Ebara/Entegris/Fujimi等|Cu recess/dishing、颗粒、低温活化、临时键合材料|产品线收入不可拆；认证长、recipe被客户保密|
|检测/量测/失效分析|设备、软件、服务、数据订阅|HB不能靠焊料自对准，void/overlay/颗粒检测价值上升|KLA、Onto、Camtek等|键合前颗粒/形貌、键合后无损界面、inline闭环|检出率/吞吐量/成本权衡；设备收入非产量|
|KGD/测试/burn-in|测试时间、设备、探针卡、测试服务|坏die进入堆叠的损失呈乘法放大|Advantest/Teradyne、OSAT测试部门、探针生态|pre-bond高覆盖、并测、HBM/存储测试、3D DFT|测试成本可能吞噬经济性，接口可达性难|
|热/基板/TIM/电源|材料、模块、共同设计|3D提高热流密度，系统客户愿为可靠TCO付费|材料/散热/基板和系统厂|背面供电、微流体/先进冷却、高导热TIM|规格碎片化、验证周期长|
|终端产品溢价|CPU/GPU/ASIC/CIS/SSD/HBM产品ASP|客户购买系统性能/TCO而非工艺本身|AMD、Sony、存储IDM、AI芯片/CSP|3D cache、near-memory、CPO和定制3D AI|最终产品需求波动；技术溢价可能被竞争压缩|

**利润捕获判断：**

- 成熟CIS/NAND中，产品IDM凭量产数据和客户资格捕获主要利润；设备材料获得稳定但难拆分的收入。
- 高端logic 3D早期，leading foundry、架构/IP/EDA与高价值产品厂捕获最大NRE和稀缺产能租；OSAT更多捕获测试、末端集成和区域化价值。
- 当流程标准化后，键合设备单机稀缺溢价可能下降，而耗材、检测、测试、软件和服务收入更经常性。
- HBM增长会直接利好DRAM、2.5D、测试、热和基板；只有原厂明确采用HB时，才将其中一部分计入HB利润池。

## 6. 竞争要素评分（定性，不是市场份额）

评分5为公开证据下的相对强项，1为证据弱/尚待产品闭环；`—`表示业务不适用。评分只用于竞争位置，不可换算销售额。

|玩家|先进节点/产品共优|HB量产学习|KGD/测试|客户生态|区域供给|公开产品闭环|综合判断|
|---|---:|---:|---:|---:|---:|---:|---|
|TSMC|5|5|4|5|4|4|高端logic 3D第一锚；透明度不足不影响能力、但限制量化|
|Intel|4|3|4|3|4|2|全栈挑战者；Direct外部客户闭环为关键|
|Samsung|5|3|4|4|5|2|协同潜力大；X-Cube产品证据需加强|
|Sony CIS|5|5|4|5|4|5|CIS赛道标杆，不是通用foundry|
|YMTC/Kioxia NAND|4|4|4|4|3|4|NAND键合路线强，Cu–Cu须逐代审计|
|ASE/Amkor/JCET|2|2–3|5|4|5|2|机会在KGD/测试/区域化；最高端前道HB受foundry挤压|
|设备头部|—|4|—|3|3|3|先行指标敏感，终端产量不可由订单推断|
|EDA/IP|—|—|3|4|4|4|轻资产高黏性，价值随流程复杂度上升|

## 7. 未来格局变化与可投资/可创业机会

### 7.1 基准格局

```text
成熟大规模：CIS W2W / NAND array–periphery bonding
        │  良率数据库、垂直IDM壁垒
        ▼
选择性高价值：logic-on-cache → logic-on-logic / near-memory
        │  D2W KGD、热/PDN、EDA、客户qualification
        ▼
期权性赛道：HBM后续代际HB / CPO / 多层3D AI
```

- **制造端继续集中：** leading foundry/IDM掌握前道晶圆、PDK和产品数据，高端3D难被纯后道快速复制。
- **OSAT不会消失，而会分工：** 在成熟2.5D/3D、测试、热、基板、区域化和客户定制中扩大；少数OSAT可能通过共同开发进入D2W。
- **设备市场先集中后分化：** 初期头部设备因验证壁垒受益；量产成熟后客户要求多来源、服务和成本，前处理/检测/耗材机会扩大。
- **终端客户话语权提高：** CSP/CPU/GPU厂通过定制ASIC、长期锁量和共同设计影响工艺选择；HBM/2.5D/HB的最优组合以系统TCO而非单一pitch决定。

### 7.2 十个可执行商业机会

1. **D2W KGD与pre-bond test:** 解决昂贵逻辑die不可返修的乘法损失。
2. **键合前表面量测与颗粒控制:** 将CMP、清洗、Cu recess/dishing和overlay连接成闭环。
3. **键合后无损界面检测:** void、delamination、open/short的高速inline检测。
4. **3D热—机械—PDN联合签核:** 为多层高功耗逻辑提供可认证模型，而非单点仿真。
5. **3D DFT和可修复/冗余:** memory/cache/buffer die分层测试、坏线隔离和yield recovery。
6. **HBM与HB共用的薄化/翘曲/搬运:** 两条路线共同需要，技术采用时间风险较低。
7. **W2W与D2W兼容的工艺服务:** W2W适合同尺寸高良率产品，D2W适合KGD/异构die；客户需要可选择平台。
8. **CPO高价值异构集成:** 先服务小量高ASP光电chiplet，重点解决热、光源和维修。
9. **区域化OSAT+安全供应:** 面向美国/欧洲/中国不同客户的IP隔离、在岸测试和长期备件。
10. **IP/FTO与本土工艺包:** DBI/HB专利映射、设计规则、材料recipe和责任边界；尤其适合新进入者缩短qualification。

### 7.3 机会排序

|机会|2026–2028确定性|2029–2031上行弹性|理由|
|---|---:|---:|---|
|KGD/测试/检测|高|高|无论TCB还是HB、2.5D还是3D都需要，且层数越高价值越大|
|CMP/清洗/表面材料|中高|高|HB放量直接增加耗材和工艺控制；客户认证形成黏性|
|3D EDA/DFT/热PDN|中高|高|设计复杂度先于大规模产量发生；轻资产、可复用|
|D2W键合设备/服务|中|很高|取决于logic 3D产品闭环，周期弹性大|
|HBM stack内HB|低至中|很高|需求池大但路线不确定；TCB仍是强替代|
|CPO直接键合|低至中|高|系统价值大但客户资格、维修和光源是瓶颈|
|单纯2.5D扩产|高|中|近期AI需求强，但竞争/CapEx和周期风险高；不属于狭义HB|

## 8. 风险、证伪条件与监控仪表盘

|假设|支持指标|证伪条件|应降级的结论|
|---|---|---|---|
|logic HB将在2027–29扩张|第二/第三个具名量产SKU、多客户设备复购、D2W良率/测试披露|到2028仍只有AMD cache类少数产品且无外部Direct SKU|从“平台扩张”降为“高价值利基”|
|HBM后续代际采用HB|DRAM厂产品工艺公告+客户qualification+量产产品映射|HBM4E/16-high继续主要TCB且性能/高度满足客户|HBM只保留邻接需求，不计HB收入|
|OSAT获得更多HB利润|具名客户D2W产品、连续季度收入、量产复购|只有项目/设备到厂，无客户产品|OSAT机会限于测试/2.5D/区域化|
|CPO在2030前实质部署|交换机/CSP产品订单、现场部署、可靠性/维修方案|仍以demo/MOU为主，无系统收入|CPO从基准情景移入上行情景|
|多来源降低TSMC集中度|Intel/Samsung/OSAT外部客户可售产品和重复订单|无外部客户、内部产品也未标Direct|TSMC生态优势保持甚至扩大|

**季度跟踪字段：**

- 具名客户/SKU/产品上市日；
- `sample / qualified / mass production / revenue`四种状态逐字区分；
- W2W/D2W/C2W、Cu–Cu/介质/TCB、bond pitch；
- pre-bond KGD覆盖率、每层yield、最终stack yield、可靠性；
- 设备首台、验收、复购、服务收入、利用率；
- 先进封装/SoIC/HB收入是否首次独立拆分；
- HBM stack层数与键合方法的原厂明示；
- second source、区域产能客户资格、客户共同公告。

## 9. 来源台账（33项）

> `A1`法定财务/监管文件；`A2`公司产品/新闻/技术页；`A4`标准/技术路线；`A5`新闻信号。以下为一手入口或既有审计台账链接。由于本子任务内置浏览器不可用，全部标“**待主控在内置浏览器重开**”；其内容只按既有证据库已核对的范围使用。

|#|来源|等级|本文可支持的最窄结论|
|---:|---|---|---|
|1|[TSMC 3DFabric](https://3dfabric.tsmc.com/english)|A2|3DFabric/SoIC/CoWoS/InFO生态存在|
|2|[TSMC SoIC](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/SoIC.htm)|A2|W2W/D2W、sub-10µm规则、3nm stacking 2025 volume-production平台措辞|
|3|[TSMC CoWoS](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/CoWoS.htm)|A2|2.5D平台存在；非HB证据|
|4|[AMD 3D Chiplet Technology](https://www.amd.com/en/corporate/events/3d-chiplet.html)|A2/A4|3D V-Cache/3D chiplet技术叙事|
|5|[AMD Ryzen 7 5800X3D launch](https://www.amd.com/en/newsroom/press-releases/2022-3-15-amd-unveils-world-s-fastest-gaming-desktop-proce.html)|A2|产品正式上市|
|6|[AMD EPYC with 3D V-Cache](https://www.amd.com/en/newsroom/press-releases/2022-3-21-amd-epyc-processors-with-amd-3d-v-cache-technol.html)|A2|server产品正式上市|
|7|[Intel Foveros](https://www.intel.com/content/www/us/en/architecture-and-technology/foveros.html)|A2/A4|一般Foveros平台|
|8|[Intel Foundry Advanced Packaging](https://www.intel.com/content/www/us/en/foundry/advanced-packaging.html)|A2|Foveros Direct/对外先进封装路线|
|9|[Intel Lakefield Hybrid Technology](https://www.intel.com/content/www/us/en/newsroom/news/intel-hybrid-technology.html)|A2|一般Foveros商业产品旁证；非Direct|
|10|[Intel Core Ultra product brief](https://www.intel.com/content/www/us/en/products/docs/processors/core-ultra/1st-gen-core-ultra-processor-brief.html)|A2|Meteor Lake/Core Ultra商业产品；非Direct证明|
|11|[Samsung Foundry Advanced Packaging](https://semiconductor.samsung.com/foundry/advanced-packaging/)|A2|X/I/H-Cube平台存在|
|12|[Samsung X-Cube technology](https://semiconductor.samsung.com/newsroom/tech-blog/x-cube-the-future-of-semiconductor-packaging-technology/)|A2/A4|X-Cube技术路线；非客户量产|
|13|[Samsung ISOCELL](https://semiconductor.samsung.com/image-sensor/)|A2|CIS产品族；逐型号HB需另证|
|14|[Sony 2-Layer Transistor Pixel announcement](https://www.sony-semicon.com/en/info/2021/202112/20211215.html)|A2/A4|stacked CIS技术|
|15|[Sony 2-Layer Transistor Pixel technology](https://www.sony-semicon.com/en/technology/mobile/2-layer-transistor-pixel.html)|A2/A4|Cu–Cu/stacked技术资料|
|16|[Sony Stacked CMOS](https://www.sony-semicon.com/en/technology/mobile/stacked-cmos.html)|A2/A4|stacked CIS路线|
|17|[YMTC Xtacking](https://www.ymtc.com/en/technology/xtacking)|A2|array/periphery分离制造和wafer bonding|
|18|[YMTC Products](https://www.ymtc.com/en/product)|A2|商业产品入口|
|19|[Kioxia 6th Gen BiCS/CBA](https://www.kioxia.com/en-jp/business/news/2020/20201020-1.html)|A2|CBA商业路线|
|20|[Kioxia BiCS FLASH](https://www.kioxia.com/en-jp/business/technology/bics-flash.html)|A2|产品/技术入口|
|21|[Micron Investor News](https://investors.micron.com/news-releases)|A1/A2|逐公告确认HBM/NAND状态|
|22|[Micron ships HBM4 samples](https://investors.micron.com/news-releases/news-release-details/micron-ships-hbm4-key-customers-power-next-gen-ai-platforms)|A2|2025年36GB、12-high、>2TB/s客户样品；非量产/HB证明|
|23|[SK hynix Investor Relations](https://news.skhynix.com/en/investor-relations/)|A1/A2|逐财报/产品公告确认HBM业务|
|24|[Samsung V-NAND/COPS](https://semiconductor.samsung.com/newsroom/tech-blog/the-technology-behind-samsungs-8th-generation-v-nand/)|A2|COPS架构；非Cu–Cu|
|25|[JEDEC HBM focus area](https://www.jedec.org/standards-documents/focus-areas/memory-configurations/hbm)|A4|HBM定义/标准背景|
|26|[Xperi DBI](https://www.xperi.com/technology/dbi/)|A2/A4|直接键合IP/技术|
|27|[EVG Hybrid Bonding](https://www.evgroup.com/technologies/hybrid-bonding/)|A2|W2W/D2W工具/工艺平台|
|28|[Besi Hybrid Bonding](https://www.besi.com/products/hybrid-bonding/)|A2|D2W设备产品线|
|29|[SUSS Advanced Packaging](https://www.suss.com/en/products-solutions/advanced-packaging)|A2|临时键合/先进封装设备生态|
|30|[KLA Advanced Packaging](https://www.kla.com/advanced-packaging)|A2|检测/量测产品生态|
|31|[Synopsys 3DIC Compiler](https://www.synopsys.com/implementation-and-signoff/3dic-compiler.html)|A2|3D EDA平台|
|32|[Cadence Integrity 3D-IC](https://www.cadence.com/en_US/home/tools/system-analysis/3d-ic.html)|A2|3D设计/分析平台|
|33|[IEEE Heterogeneous Integration Roadmap](https://eps.ieee.org/technology/heterogeneous-integration-roadmap.html)|A4|异构集成技术背景；非产品/出货证据|

## 10. 交给监工的六条可质询命题

1. **D1/口径：** HBM和2.5D是3D IC/HB的需求邻接池，不可并入狭义HB销售额；请审计总报告是否重复计数。
2. **D2/玩家：** TSMC相对领先是能力/生态判断，不是公开份额；请删除任何由CoWoS WPM推SoIC WPM的换算。
3. **D3/路线：** Intel Foveros商业化不等于Foveros Direct商业化；Samsung X-Cube平台不等于客户Cu–Cu量产。
4. **D4/年度：** 2027–2031全部为A6条件情景；若总报告改成厂商承诺、销量规划或确定性事件，应判P0/P1。
5. **D5/客户起量：** 样品、tape-out、设备到厂、qualification均不是销售；只有具名可售SKU/稳定交付/收入进入实际起量。
6. **D6/来源：** 本子任务未能重新打开网页；所有来源须由主控内置浏览器复核发布日期与原文，尤其SoIC的3nm/2025措辞和Micron HBM4样品规格。

## 11. 最终判断

2026–2031的3D IC商业机会不是“所有AI芯片都转混合键合”，而是三条逐级扩张的曲线：成熟CIS/NAND提供规模和工艺学习；logic-on-cache向精选logic-on-logic/near-memory提供最高单位价值；HBM后续代际和CPO提供高弹性期权。TSMC、Intel、Samsung、Sony、存储IDM和OSAT不会在一个统一市场里同维度竞争，而是在前道工艺、产品架构、客户资格、测试/良率和区域供给上分层竞争。

最可信的商业策略是优先布局路线共用的“卖铲子”环节——KGD/测试、检测、CMP/清洗、翘曲/薄化、热/PDN和3D EDA——同时把D2W键合设备、HBM stack内HB和CPO视为需要产品闭环验证的高弹性机会。任何销量/产能模型都应由实际可售产品、客户qualification和可用产能驱动，不能由平台名称、CapEx、设备订单、HBM收入或CoWoS产能反推。
