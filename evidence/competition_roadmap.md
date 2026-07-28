# Hybrid Bonding 竞争格局、客户需求与 2025–2031 路线图（E 组）

**研究日期：** 2026-07-28  
**范围：** Cu–Cu / dielectric hybrid bonding（直接混合键合）及直接竞争的 TSV + micro-bump/TCB、2.5D interposer/RDL、单片式 3D（monolithic 3D）和传统封装路线。覆盖制造平台、OSAT、设备/材料/EDA 生态，以及 CIS、3D NAND、logic/cache、HBM、photonics、MEMS 的应用需求。  
**证据纪律：** 本稿仅在公司产品、公告、年报/监管披露、标准和技术资料的限定范围内作判断。公开资料没有可比较、同口径的 hybrid-bonded die/package/wafer 出货量和收入份额，因而**不编造市场份额或 2025–2031 精确数量预测**。所有“领先/份额”仅作能力与商业化状态的定性判断。

**浏览器说明：** 本轮按用户要求只尝试隔离内置浏览器；执行环境返回 `Browser is not available: iab`。未使用桌面 Chrome、个人会话或 Cookie。文末保留一手 URL 台账供主控逐页复核；本轮不能重新打开的网页，不将细节升级为实物出货或客户事实。

---

## 一、执行结论

### 1. 这不是一个统一市场，而是六个工艺—客户市场

`hybrid bonding` 是制造工艺，不是一种终端产品。因此竞争格局应以“谁能在何种 die 类型、何种键合模式、何种良率和客户资格下交付”为单位，而不是以一个笼统的全球份额描述。

|应用赛道|截至 2025–2026 的商业成熟度|主要客户价值|混合键合的真实替代物|2025–2031 最关键转折|
|---|---|---|---|---|
|CIS|成熟商业化，最久经验证的直接键合类应用|像素/逻辑分别优化、面积、读出、低噪声|传统 stacked CIS、TSV/微凸点、像素工艺改进|更大像素阵列、global shutter、汽车/工业可靠性与边缘 AI 读出|
|3D NAND|垂直架构与 array–CMOS 分离/键合已大规模商业化；Cu–Cu 机制须逐代确认|bit density、periphery 缩放、成本/层数扩展|单晶圆 CMOS-under-array、string-stack/etch 优化|层数堆叠难度上升、wafer bonding 良率和成本、QLC/PLC/enterprise SSD 周期|
|logic-on-cache / logic-on-logic|AMD 3D V-Cache 是强商业例；更细 pitch logic 3D 仍是选择性导入|带宽、latency、cache capacity、能效、die disaggregation|2D cache、chiplet 2.5D、micro-bump 3D、先进节点单 die|D2W KGD、背面供电/热、设计签核、CPU/AI 客户规模 qualification|
|HBM / memory-on-logic|HBM 商业规模很大；混合键合在 HBM stack/logic 接口的实际采用不能一概而论|带宽、功耗、容量、系统集成|TSV + micro-bump + TCB、2.5D interposer/RDL|HBM4/后续代际、base-die 变化、热与测试；不是“HBM4 必然全切 hybrid bond”|
|硅光/photonic|技术和产品导入并行，直接键合更可能在高价值对准/异构集成场景增长|光源/调制器/探测器与 CMOS 集成、能耗、带宽密度|co-packaged optics、flip-chip、被动/主动对准、外置光模块|AI 网络带宽、激光器/III-V 集成良率、封装热和可靠性资格|
|MEMS|特定结构成熟，更多由器件设计与真空腔/传感可靠性决定|小型化、低寄生、封装可靠性|wafer bonding、anodic/eutectic/adhesive bonding、TSV|汽车/工业 qualification、传感器融合、成本和长期供给|

### 2. 最强的已商业化案例与最容易被误写的案例

- **可以稳健写为商业产品/实际供货路线的：** Sony 等堆叠 CIS；YMTC Xtacking / Kioxia CBA 等 3D NAND array–periphery 分离/键合架构；AMD 3D V-Cache 的 CPU/server 产品（与 TSMC SoIC 3D 集成生态相关）。
- **可以稳健写为已商业化 3D/先进封装、但不可自动写为 direct hybrid bond 的：** Intel Foveros 的一般产品、HBM TSV stack、CoWoS/EMIB/I-Cube/H-Cube 等 2.5D 系统集成、3D NAND 中未逐代披露 Cu–Cu/oxide 界面的架构。
- **可以写为路线图/导入候选，但不能称量产份额的：** Intel Foveros Direct、Samsung X-Cube 的特定客户产品、HBM4 内部/外部 direct bonding、AI logic-on-logic、CPO/光电异构直接键合。

### 3. 竞争的本质是“系统良率 + 客户资格”，不是单一键合机

技术竞争要素依次是：表面平坦度和污染控制、overlay、D2W KGD、薄化与翘曲、键合后无损检测、热/供电、测试与可修复性、3D EDA/PDK/签核、材料和设备可得性、最后才是客户长期 qualification。工具、论文或专利能证明技术参与，不证明商业客户、稳定良率或实际出货。

---

## 二、竞争坐标：制造平台、记忆厂与产品客户

### 2.1 制造平台的定性位置（不报虚假份额）

|平台/公司|主要技术/产品名|公开的直接键合/3D 集成证据|当前商业状态|客户与收入可得性|竞争位置与限制|
|---|---|---|---|---|---|
|TSMC|SoIC®、3DFabric、CoWoS®、InFO®|SoIC 是正式 3D 集成产品平台，服务 W2W/D2W 等 3D 集成；CoWoS/InFO 属不同层级先进封装|SoIC 平台商业可用；AMD 3D V-Cache 是明确的产品生态例子；各客户/SKU模式未公开|TSMC 不按 SoIC/CoWoS package、die、客户拆分实际收入或出货|**高端 foundry/系统封装能力锚。** 优势是逻辑、3D/2.5D、生态与客户协同；限制是公开数据无法计算 SoIC 份额或产品量。|
|Intel|Foveros、Foveros Direct、EMIB|一般 Foveros 已进入 Lakefield/Meteor Lake 等产品；Direct 是更细 pitch 直接键合路线|Foveros 已商用；Foveros Direct 的逐产品量产客户闭环未取得|Intel 业务/Foundry 披露不分 Foveros Direct 收入、die或客户量|**全栈挑战者。** 自有产品可提供学习曲线，Foundry 对外采用是关键转折；不可把 Foveros 总出货等于 Direct。|
|Samsung Foundry / DS|X-Cube、I-Cube、H-Cube、ISOCELL|X-Cube 公开为 3D IC/先进封装平台；I/H-Cube 面向系统集成；堆叠 CIS 商业化|平台与 CIS 产品存在；单个 X-Cube Cu–Cu 客户/SKU 量产未被公开一手资料充分确认|DS/Foundry收入不拆分平台，客户/出货不可得|**存储—逻辑—封装协同候选。** 关键是把平台规格转成客户 qualification 与实际设计赢。|
|Sony Semiconductor Solutions|Exmor RS / stacked CIS / two-layer transistor pixel|公开技术资料描述 stacked CMOS 与 Cu–Cu connection；CIS 产品长期销售|CIS 是成熟商业化应用；并不披露按直接键合分拆的出货/收入|sensor 总量、客户组合和每代互连机制未完全公开|**CIS 直接键合的商业标杆。** 优势是垂直整合、影像客户认证；非通用 foundry/AI packaging 替代者。|
|YMTC|Xtacking®|array wafer 与 peripheral CMOS wafer 独立制造并通过 wafer bonding 集成的公开架构|多代 NAND 技术/产品路线已商业化|不披露特定键合机理的 NAND die/wafer 实物数量|**中国 3D NAND 分离制造/键合路线代表。** 对“是否 Cu–Cu hybrid bond”须逐代工艺文件审计。|
|Kioxia|CBA（CMOS directly Bonded to Array）/BiCS FLASH|CBA 架构为公司公开产品技术路线|商业 NAND 产品路线|不按 CBA/键合方式披露收入与出货|**全球 array–CMOS direct bonding 重要参与者。** CBA 不能自动推为 Cu–Cu/oxide hybrid bond 每层出货。|
|Micron|CuA（CMOS-under-Array）、3D NAND；HBM|CuA 是 array/periphery 布局架构；公司 HBM/NAND 商业收入可由财报/公告确认|3D NAND/HBM 均商业化|不披露“CuA direct bond”或 hybrid-bond stack 的单位出货|**高端存储重要竞争者。** CuA 不是 Cu–Cu bonding 的证据；HBM 销量不等于 hybrid-bonded HBM。|
|SK hynix|4D NAND、HBM、CIS/logic 投资|4D NAND 为产品架构；HBM/3D NAND 均有商业产品|产品层面量产/收入可确认，但 direct bond 结构要逐产品核验|未按 hybrid bonding 拆分|**HBM/NAND 竞争强者。** 决定因素是 HBM客户认证与存储制造，不应被混合键合概念替代。|

### 2.2 OSAT 的角色：能承接什么，不能承接什么

|类别|主要参与者|在 hybrid bonding 中的现实角色|关键客户需求|证据与竞争边界|
|---|---|---|---|---|
|领先 OSAT|ASE、Amkor、JCET、PTI、ChipMOS 等|先进封装、RDL/FC/2.5D、测试、KGD、热和可靠性；部分拥有/导入高密度键合能力|量产良率、测试覆盖、可靠性、客户 IP/数据安全、区域化供应|OSAT 平台或项目公告不能证明其已经大规模生产 Cu–Cu direct-bond die。应逐产品确认 D2W/W2W、客户 qualification 和收入。|
|垂直整合 IDM/foundry 内部封装|Sony、TSMC、Intel、Samsung、存储 IDM|最先获得产品—工艺共优化、良率学习和高价值产品资料|产品设计协同、内部 KGD/测试、供应连续性|这一模式在 CIS、NAND、CPU cache 更有优势；外部 OSAT 要追赶需同时补设备、工艺、PDK/设计协同和客户认证。|
|测试与可靠性|PTI、ASE/Amkor测试部门、Advantest/Teradyne生态|pre-bond KGD、post-bond 测试、burn-in、失效分析是不可省略环节|更高并测、热、测试时间、可追溯性|测试设备/厂商收入不能反推 hybrid-bonded die 数；但测试是否可用决定量产爬坡。|

**竞争判断：** 对最高端逻辑—缓存/逻辑—逻辑 D2W 直接键合，OSAT 的竞争不是“能否购买设备”，而是能否获得客户的 design enablement、前道晶圆协同、KGD、可靠性数据库和连续量产资格。在区域供应链重构中，Amkor Arizona、ASE/JCET 的先进封测项目具有战略价值，但项目宣布/建设/设备到厂不等于已形成 direct-bonding 有效产能。

---

## 三、按应用赛道的需求驱动、渗透节奏与路线替代

### 3.1 CIS：成熟市场的性能—成本平衡，而不是 AI/HBM 逻辑

|问题|2025–2026 状态|2027–2029 可能转折|2030–2031 方向判断（A6）|客户资格/壁垒|
|---|---|---|---|---|
|需求驱动|手机影像、车载、工业、安防、XR；更多像素/高速读出/低噪声与 ISP/AI功能|高动态范围、global shutter、车规可靠性、计算摄影与边缘处理集成|更高堆叠密度和像素/逻辑分工继续，但并不必然变成通用 AI hybrid-bond market|光学、像素质量、暗电流、良率、供应连续性和终端 OEM qualification。|
|直接键合渗透|Sony 的 stacked CIS/Cu connection 是成熟例证；同业逐型号机制不同|更小 pixel pitch 与逻辑功能增加会提高高密度垂直连接价值|主要受产品架构/成本而非单纯 pitch 决定|CIS 可靠性、图像质量、摄像头模组、客户验证周期长；既有供应商壁垒高。|
|替代路线|传统 stacked CIS、TSV/微凸点、像素工艺优化、2D logic集成|技术选择取决于良率、sensor面积、热和成本|direct bonding 不会在所有低端 CIS 中替代成本更低路径|不是所有“stacked”都需要或采用 Cu–Cu direct bonding。|

### 3.2 3D NAND：面向成本和 bit density 的规模化竞争

|问题|2025–2026 状态|2027–2029 可能转折|2030–2031 方向判断（A6）|客户资格/壁垒|
|---|---|---|---|---|
|需求驱动|enterprise SSD、云、手机、PC、消费存储的容量/成本周期|层数增加带来高深宽比刻蚀、string stack、periphery 面积和良率挑战；array–CMOS 分离/键合的价值上升|存储价格周期与技术成本共同决定键合架构渗透；不能按 AI capex 外推|SSD controller/firmware、企业客户认证、耐久性、供应稳定与成本/bit。|
|直接键合渗透|Xtacking/CBA 已证明 array–periphery 分离/键合可商用|逐代确认键合界面、材料和良率，避免品牌名替代工艺事实|“3D NAND 键合”与 AI logic direct bonding 的设备/良率要求部分共同、商业单位不同|NAND 厂在设备/材料/良率上的多年积累形成高门槛。|
|替代路线|CMOS-under-array、string-stack、单晶圆工艺、层数和 cell architecture 优化|不同 IDM 的技术路线竞争并存|无统一路线赢家，关键是 cost per bit 与 yield|不能将 CuA/COPS/4D 等名称全部视为 Cu–Cu hybrid bonding。|

### 3.3 logic-on-cache / logic-on-logic：未来价值密度最高、资格最严的赛道

|问题|2025–2026 状态|2027–2029 可能转折|2030–2031 方向判断（A6）|客户资格/壁垒|
|---|---|---|---|---|
|需求驱动|AI/数据库/游戏/高性能计算受 memory wall、latency、power限制；AMD V-Cache 是商业模板|更大 cache、异构 chiplet、backside power、D2W KGD、热管理和软件协同|若良率、热和设计生态收敛，逻辑 3D 的渗透可上升；否则 2.5D/chiplet延续|高价值逻辑 die、功能安全、性能一致性、软件生态、长期供货；客户切换成本极高。|
|直接键合渗透|AMD/TSMC 已证明 cache-on-logic 可进入标准产品；Intel/TSMC/Samsung 各有路线|从 cache 向 logic-on-logic 扩展，需要在高功耗/高频下验证 PDN、热、时序和可测试性|不应预设所有 CPU/GPU转向 direct bond；产品设计和收益必须覆盖制造成本|最强壁垒是与 logic PDK、EDA、测试、CPU/AI architecture 的共同优化，而不是单一设备。|
|替代路线|更大单 die、2D cache、2.5D chiplet、micro-bump 3D、先进节点缩放、optical/interconnect优化|各路线可并存，取决于 bandwidth/latency/成本/良率|monolithic 3D 或更小 pitch direct bonding是远期候选，不是当前普遍商业事实|不能用“技术上更先进”替代产品 ROI 和客户 qualification。|

### 3.4 HBM 与 memory-on-logic：最大需求池，但混合键合不是默认接口

|问题|2025–2026 状态|2027–2029 可能转折|2030–2031 方向判断（A6）|客户资格/壁垒|
|---|---|---|---|---|
|需求驱动|AI training/inference、HPC 对 memory bandwidth 的刚性需求；HBM与2.5D封装/基板/热共同扩张|HBM4/后续代际的 I/O、logic base die、容量、散热、测试和供给分配|HBM持续增长但产品工艺不应由路线图预先写死|DRAM 良率、TSV、stack、KGD、封装、base die、客户认证和供应分配。|
|混合键合位置|可能用于部分高密度 memory-on-logic 或特定 stack/interface；公开证据不足以宣布主流全面切换|TCB/micro-bump 与 direct bonding 并行，是否采用由 DRAM厂/客户/SKU决定|更小 pitch 的经济动机上升，真正转折需以供应商量产/客户qualification实证|HBM qualification 对性能、功耗、热、可靠性、测试与持续供给要求最高。|
|替代路线|TSV + micro-bump + TCB；2.5D silicon/RDL interposer；更宽接口/更高pin speed；cache层次优化|HBM4 不是唯一方案，系统可通过更多/更大 stack、CXL/DDR/cache等缓解|不会由单一键合方式决定系统胜负|将 HBM收入、stack 数或CoWoS capacity换算为 hybrid-bonded 量均属禁用推断。|

### 3.5 Photonics/CPO：高潜力，但从器件演示到系统资格的鸿沟最大

|问题|2025–2026 状态|2027–2029 可能转折|2030–2031 方向判断（A6）|客户资格/壁垒|
|---|---|---|---|---|
|需求驱动|AI cluster 网络带宽、交换芯片 I/O、功耗/距离限制|CPO、硅光、外置激光器、光电 chiplet的系统热、维修和可制造性决定是否放量|如果 AI 网络的电互连功耗成为系统瓶颈，高密度异构集成/键合价值明显上升|电—光协同、激光器/III-V材料、对准、封装热、现场可维修性与超大客户qualification。|
|混合键合位置|适合高密度、低寄生的电子—光子/逻辑—photonic异构连接，但并非所有CPO必须用Cu–Cu direct bond|产品导入需跨材料/晶圆厂/封装厂/网络客户共同开发|可能在高价值、低量先起量，后取决于生态标准化|目前公开资料常是演示、平台或合作，不能直接当作商业 volume。|
|替代路线|flip-chip、micro-bump、主动对准、传统光模块、可插拔光互连|谁在成本、热、良率、维修性上胜出谁获得采用|不会只由带宽数字决定|客户对数据中心维护方式和供应链的改变是主要障碍。|

### 3.6 MEMS：相对稳定的小型化与封装可靠性市场

|问题|2025–2026 状态|2027–2029 可能转折|2030–2031 方向判断（A6）|客户资格/壁垒|
|---|---|---|---|---|
|需求驱动|消费电子、汽车、工业、医疗、惯导和环境感知|自动驾驶/工业安全推动可靠性与低漂移；传感器融合增加集成需求|直接键合会在高价值/高可靠器件持续渗透，但非所有MEMS都适合|真空腔、应力、漂移、车规可靠性、成本与长期供货。|
|替代路线|anodic/eutectic/adhesive bonding、TSV、wafer-level packaging|不同MEMS结构对材料/热预算依赖很强|通用“hybrid bonding份额”没有可比意义|不能将 CIS 的商业化节奏直接复制到 MEMS。|

---

## 四、制造路线图：主要玩家的可核验 roadmap 与转折点

### 4.1 TSMC

|维度|可写路线|状态|关键转折/需追踪证据|
|---|---|---|---|
|SoIC|3DFabric 下的 3D 集成平台，连接 W2W/D2W 设计、先进逻辑和封装协同|A2 平台已商业可用|客户产品何时公开映射 SoIC；是否披露实际收入/规模；D2W KGD、背面供电、热和测试。|
|CoWoS/InFO|主流 AI/HPC 系统封装路线|A2 商业平台|容量、基板、HBM、热、测试和客户交期；**不是**混合键合出货量。|
|关键风险|良率/产能/客户分配和供应链|方向判断|不能用公开先进封装营收、CapEx或WPM推 SoIC/Hybrid Bond units。|

**转折点：** 从单一逻辑—缓存的产品证明向更高功耗、更多 die、D2W KGD 与 3D 系统设计的可重复量产；不是某次 3DFabric 版本发布。

### 4.2 Intel

|维度|可写路线|状态|关键转折/需追踪证据|
|---|---|---|
|Foveros|已用于商业产品的 3D packaging 技术|A2 产品商业化|产品层面继续证明相同/新一代工艺的性能、良率和供应。|
|Foveros Direct|更细 pitch 的 direct bonding 路线|A2/A4 平台/技术|必须等待 Intel 或客户公开“某 SKU 使用 Foveros Direct 并已量产/出货”的闭环。|
|EMIB|2.5D bridge，重要但不是 hybrid bonding|A2平台|与 Foveros Direct 的共封装组合可能提高价值，但不能合并统计。|
|Foundry|把先进封装作为对外服务|A2服务定位|外部客户 design win、产品资格、产能/收入的独立披露；总Foundry收入无替代作用。|

**转折点：** 不是有 Foveros 产品，而是 Foveros Direct 在外部客户或新产品实现可确认的量产、可靠性和客户资格。

### 4.3 Samsung

|维度|可写路线|状态|关键转折/需追踪证据|
|---|---|---|
|X-Cube|3D IC/TSV 先进封装平台|A2 平台|明确 W2W/D2W/Cu–Cu机制、客户SKU、可售状态与商业收入。|
|I-Cube/H-Cube|2.5D/高密度异构封装平台|A2平台|HBM/logic系统的客户认证、基板/热/测试和供应连续性。|
|CIS|ISOCELL 堆叠产品|A2产品|逐代键合机制而非总产品量。|
|存储—逻辑协同|同一集团覆盖存储、foundry与封装|A2商业能力|真正的高端客户认证，而非概念整合。|

**转折点：** X-Cube 的技术路线能否转化为被客户点名、可量产的直键合产品；HBM 产品和封装平台不能自动互相证明。

### 4.4 Sony、YMTC、Kioxia、Micron、SK hynix

|公司|路线|当前状态|2025–2031 转折点|
|---|---|---|---|
|Sony|CIS direct Cu connection/stacked sensor|成熟商用、长期客户资格|更多堆叠层/逻辑功能、车载与工业可靠性；可持续量产比“更小pitch”更重要。|
|YMTC|Xtacking array–periphery wafer bonding|NAND产品路线商业化|更高层数、设备/材料可得性、良率/成本和客户SSD认证；须逐代核实是否Cu–Cu。|
|Kioxia|CBA|NAND产品路线商业化|BiCS代际与成本/bit、enterprise需求；CBA名称不替代具体直接键合机制。|
|Micron|CuA 3D NAND、HBM|NAND/HBM商业化|HBM客户认证/供给与NAND周期各自独立；CuA不应被误认作Cu–Cu hybrid bond。|
|SK hynix|4D NAND、HBM|NAND/HBM商业化|HBM后续代际和客户分配；NAND高层数/成本。不能从两者推hybrid bonding份额。|

---

## 五、客户需求、资格和商业壁垒

### 5.1 客户为什么购买 direct hybrid bonding，而不是“更先进就买”

|客户诉求|CIS/NAND|logic/cache/AI|HBM/系统封装|photonics/MEMS|
|---|---|---|---|---|
|性能/带宽|读出速度、像素功能；NAND架构效率|cache bandwidth/latency、chiplet效率|带宽、功耗、I/O密度|光电I/O或传感性能|
|成本|每颗sensor/每bit成本、良率|高价值die的性能收益必须覆盖良率/封装成本|系统成本、HBM供给、基板/热|模块成本、装调/维修成本|
|可靠性|手机/车规/工业成像|服务器/数据中心长期运行|热循环、测试、供应连续性|光/机/电稳定性、汽车/工业寿命|
|供应链|垂直IDM与模组客户|foundry/OSAT/EDA/IP共开发|DRAM厂、逻辑厂、封装、基板和系统客户|材料、光源、封装、网络/终端客户|

### 5.2 客户 qualification 的四道门

1. **工艺资格：** 表面、对准、键合、薄化、缺陷、可靠性，不能只看实验 die。  
2. **产品资格：** KGD、pre/post-bond test、性能、热、功耗、寿命和失效模式。  
3. **系统资格：** 软件/固件、内存一致性、网络/光学互连、散热、电源和维修策略。  
4. **供应资格：** second source、地域、设备/材料备件、数据安全、长期成本和交付节奏。

没有完成四道门，样品、专利、客户合作、设备订单或“ready for production”都不能视作稳定起量。

### 5.3 竞争壁垒的分层

|壁垒|为何难复制|领先者常见优势|后来者的必要补课|
|---|---|---|---|
|产品—工艺协同|架构选择决定热、测试、die切分和互连|Sony CIS、TSMC/AMD、Intel自用产品、存储IDM|拿到客户设计资料和共同开发窗口。|
|良率数据和失效分析|直接键合不可返修，缺陷代价放大|量产历史、材料/设备调参、数据库|工程批、可靠性、测试、失效闭环。|
|D2W KGD/测试|高价值die不能靠“先堆后测”承受损失|foundry/IDM内部测试和设计控制|pre-bond coverage、probe/测试时间、test economics。|
|EDA/PDK/IP|3D热/应力/PDN/SI/DFT签核需全栈模型|foundry PDK、软件工具、客户流程|工具许可、本土替代、流程认证和责任边界。|
|材料/设备供应|CMP、清洗、键合、检测彼此耦合|合格供应商、服务/备件、长期联合开发|取得设备、维护、材料认证和可重复工艺。|
|客户认证与商业规模|终端客户承担系统风险，不轻易切换|已有量产SKU、供应连续性、品牌可信度|从样品到design win再到持续订单的多年周期。|

---

## 六、替代路线：什么时候不应选择混合键合？

|路线|最适用条件|相对 hybrid bonding 的优势|主要限制|竞争含义|
|---|---|---|---|---|
|TCB + micro-bump|HBM、成熟3D package、较大pitch、成本/良率优先|供应链成熟、可用设备/测试生态广、已验证量产|pitch/寄生/密度受限，热和高度管理仍复杂|在 2025–2028 仍是强替代路线，不能被路线图提前淘汰。|
|2.5D interposer/RDL/bridge|多大die + HBM 横向集成、系统封装|KGD更容易、设计和维修风险相对低、生态成熟|面积、基板、互连距离、成本和热|CoWoS/EMIB/I-Cube/H-Cube 是直键合的互补或替代，不应被混为同一市场。|
|monolithic 3D|极小互连/高密度逻辑层，允许前端工艺共优化|理论密度和延迟优势强|热预算、工艺复杂、EDA/测试、产品成熟度|远期竞争方向，现阶段不能与商用D2W产品按同一收入/出货口径比较。|
|更大单 die/先进节点|收益可由制程缩放或架构优化获得|避免3D封装/键合的良率与测试复杂度|reticle、成本、功耗和memory wall|若3D的系统收益不足，客户会选择此路径。|
|CXL/DDR/cache hierarchy|系统可通过更远存储层缓解容量需求|降低对高价近存储的依赖|latency/bandwidth不等价于HBM/3D cache|memory-on-logic需求不能只由总AI算力推断。|

---

## 七、2025–2031 竞争格局情景（非出货预测）

### 基准情景：多赛道并行，CIS/NAND成熟，logic/cache选择性扩大

- **2025–2026：** CIS、3D NAND array–CMOS 架构、AMD 3D V-Cache 提供最清晰的商业案例；AI/HBM 驱动先进封装全链投资，但主流系统交付仍大量依赖 TCB/micro-bump、2.5D interposer/RDL 和成熟封装。
- **2027–2028：** 直接键合的价值从 “单一高价值 cache/传感器” 向更多 logic/cache、部分 AI chiplet 和光电异构集成扩展，前提是 D2W KGD、热/PDN、测试与客户 qualification 同时过关。HBM4 的转折是接口/系统协同，不预设普遍键合工艺切换。
- **2029–2031：** 若高密度逻辑3D、CPO、后续 HBM/memory-on-logic 完成重复性量产，direct bonding 的单位价值可能显著提高；若良率、热或设计生态不能收敛，则微凸点/TCB、2.5D和更传统封装继续长期并存。

### 上行情景

- 高端 AI 推理对 latency/energy 的价值提高，3D cache 和 logic-on-logic 的 ROI 超过直接制造风险；
- CPO 在大规模 AI 网络中进入实质部署，带动电子—光子高密度异构集成；
- D2W KGD、检测、EDA/DFT 和后段测试形成标准化、可复制的设计—制造闭环；
- 多家 foundry/IDM/OSAT 获得客户产品级 qualification，减少单一供给点集中度。

### 下行情景

- AI 需求延续，但 HBM/2.5D/TCB 通过扩产和产品优化充分满足系统要求，direct bond 的边际收益不足；
- 高价值逻辑 die 的直接键合良率、热或不可返修风险超出产品经济性；
- 光电 CPO 因可维护性、激光器/封装和客户部署节奏慢于预期；
- 设备、材料、EDA、测试和人才的同时性约束拉长客户端 qualification。

**审计限制：** 上述仅是技术—商业情景，不是 2025–2031 的 wafer、die、package、HBM stack 或市场收入预测。公开数据不足时，方向判断优于伪精确 CAGR。

---

## 八、份额、收入和实际出货：哪些数据可以写，哪些必须留空

|字段|当前可得性|总报告写法|
|---|---|---|
|全球 hybrid-bonded die/wafer/package 实物出货|各公司普遍未披露，无法同口径加总|留空；不得以收入/设备订单/厂房推回。|
|按 CIS/NAND/logic/HBM/photonics/MEMS 的混合键合收入份额|无同口径公开统计|仅做定性成熟度和竞争位置比较。|
|AMD 3D V-Cache 产品是否商业销售|有公司产品公告|可写 A2“正式上市/可售”；不写单SKU销量/SoIC die量。|
|Sony stacked CIS 是否商业化|有公司产品/技术资料|可写成熟产品技术；不写按Cu–Cu拆分出货。|
|TSMC/Intel/Samsung 平台是否存在|有公司产品平台资料|可写 A2平台；不能写客户出货/份额。|
|Micron/SK hynix/Samsung HBM收入或产品状态|逐公司财报/公告可有A1/A2|只能写其原始收入/产品状态；不能换算 hybrid bonding volume。|
|设备商订单和收入|财报可有A1|只能用于设备周期；不是终端direct-bond产品产量。|

---

## 九、主报告可直接采用的最终判断

> Hybrid bonding 的商业化并非一条单线：Sony 等堆叠 CIS、YMTC Xtacking/Kioxia CBA 等 3D NAND array–CMOS 分离/键合架构，以及 AMD 3D V-Cache 对应的 logic-on-cache 产品，分别代表已被市场验证的传感、存储和高性能逻辑应用。它们的共同点是高价值的垂直互连收益足以覆盖更复杂的制造与良率控制；不同点是键合对象、是否采用 Cu–Cu、W2W/D2W方式、测试、热和客户资格完全不同。

> 2025–2031 的竞争不应被简化为“谁有键合机”或“HBM4 是否使用 hybrid bonding”。TSMC、Intel、Samsung 的优势在逻辑/封装平台和客户生态；Sony、YMTC、Kioxia、Micron、SK hynix 的优势在垂直产品和存储/传感器制造学习曲线；OSAT 的机会在把先进封装、KGD、测试、可靠性与区域供应链交付做成可认证的服务。直接键合的真正扩张要以产品级量产、良率、热/测试和客户 qualification 为证，而不是设备订单、工艺演示或路线图。

---

## 附录 A：一手 URL 台账（至少 20 项）

下列链接是本研究的原始来源入口。其证据等级仅覆盖表中说明的事项；网页存在不等于产品实际出货或收入已公开。

|#|公司/机构|来源|状态/可用范围|
|---:|---|---|---|
|1|TSMC|[3DFabric](https://3dfabric.tsmc.com/english)|A2，SoIC/CoWoS/InFO平台|
|2|TSMC|[SoIC](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/SoIC.htm)|A2，3D 集成平台|
|3|TSMC|[CoWoS](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/CoWoS.htm)|A2，2.5D 平台，非自动 hybrid bonding|
|4|AMD|[3D Chiplet Technology](https://www.amd.com/en/corporate/events/3d-chiplet.html)|A2/A4，3D V-Cache技术叙事|
|5|AMD|[Ryzen 7 5800X3D launch](https://www.amd.com/en/newsroom/press-releases/2022-3-15-amd-unveils-world-s-fastest-gaming-desktop-proce.html)|A2，产品正式上市|
|6|AMD|[EPYC 3D V-Cache launch](https://www.amd.com/en/newsroom/press-releases/2022-3-21-amd-epyc-processors-with-amd-3d-v-cache-technol.html)|A2，产品正式上市|
|7|Intel|[Foveros](https://www.intel.com/content/www/us/en/architecture-and-technology/foveros.html)|A2/A4，技术平台|
|8|Intel|[Foundry Advanced Packaging](https://www.intel.com/content/www/us/en/foundry/advanced-packaging.html)|A2，服务/路线平台|
|9|Intel|[Lakefield / Hybrid Technology](https://www.intel.com/content/www/us/en/newsroom/news/intel-hybrid-technology.html)|A2，Foveros 产品线旁证|
|10|Samsung|[Foundry Advanced Packaging](https://semiconductor.samsung.com/foundry/advanced-packaging/)|A2，X-Cube/I-Cube/H-Cube平台|
|11|Samsung|[ISOCELL](https://semiconductor.samsung.com/image-sensor/)|A2，商用图像传感器产品|
|12|Sony|[2-Layer Transistor Pixel announcement](https://www.sony-semicon.com/en/info/2021/202112/20211215.html)|A2/A4，stacked CIS技术|
|13|Sony|[2-Layer Transistor Pixel technology](https://www.sony-semicon.com/en/technology/mobile/2-layer-transistor-pixel.html)|A2/A4，Cu–Cu/stacked技术资料|
|14|Sony|[Stacked CMOS technology](https://www.sony-semicon.com/en/technology/mobile/stacked-cmos.html)|A2/A4，stacked CIS路线|
|15|YMTC|[Xtacking® technology](https://www.ymtc.com/en/technology/xtacking)|A2，array–periphery wafer bonding架构|
|16|YMTC|[Products](https://www.ymtc.com/en/product)|A2，产品入口|
|17|Kioxia|[6th Gen BiCS FLASH / CBA announcement](https://www.kioxia.com/en-jp/business/news/2020/20201020-1.html)|A2，CBA商业路线|
|18|Kioxia|[BiCS FLASH](https://www.kioxia.com/en-jp/business/technology/bics-flash.html)|A2，技术入口|
|19|Micron|[3D NAND](https://www.micron.com/products/nand-flash/3d-nand)|A2，3D NAND产品路线|
|20|Micron|[Investor news releases](https://investors.micron.com/news-releases)|A1/A2，HBM/NAND收入或产品状态应逐公告读取|
|21|SK hynix|[Flash Memory news](https://news.skhynix.com/en/category/product/flash-memory/)|A2，NAND产品路线|
|22|SK hynix|[Investor Relations](https://news.skhynix.com/en/investor-relations/)|A1/A2，财务/产品信息逐文件读取|
|23|Samsung|[V-NAND technology / COPS](https://semiconductor.samsung.com/newsroom/tech-blog/the-technology-behind-samsungs-8th-generation-v-nand/)|A2，COPS技术路线|
|24|Xperi|[DBI Direct Bond Interconnect](https://www.xperi.com/technology/dbi/)|A2/A4，直接键合IP/技术|
|25|EV Group|[Hybrid Bonding](https://www.evgroup.com/technologies/hybrid-bonding/)|A2，设备/工艺平台|
|26|Besi|[Hybrid Bonding](https://www.besi.com/products/hybrid-bonding/)|A2，设备平台|
|27|SUSS MicroTec|[Advanced Packaging](https://www.suss.com/en/products-solutions/advanced-packaging)|A2，设备平台|
|28|ASMPT|[Advanced Packaging](https://www.asmpt.com/en/products/advanced-packaging/)|A2，封装设备生态|
|29|KLA|[Advanced Packaging](https://www.kla.com/advanced-packaging)|A2，检测/量测生态|
|30|Synopsys|[3DIC Compiler](https://www.synopsys.com/implementation-and-signoff/3dic-compiler.html)|A2，3D EDA|
|31|Cadence|[Integrity 3D-IC](https://www.cadence.com/en_US/home/tools/system-analysis/3d-ic.html)|A2，3D EDA|
|32|JEDEC|[HBM focus area](https://www.jedec.org/standards-documents/focus-areas/memory-configurations/hbm)|A4，HBM定义；非产品证据|
|33|IEEE|[Heterogeneous Integration Roadmap](https://eps.ieee.org/technology/heterogeneous-integration-roadmap.html)|A4，工艺/产业技术背景|

## 附录 B：发布前强制复核清单

1. 对每条 URL 重开并记录发布日期、访问日、网页存档/PDF；
2. 将“hybrid bonding / Cu–Cu / oxide bonding”逐字核对，不把 `stacked`、`3D`、`CBA`、`CuA`、`Foveros`、`CoWoS` 自动升级；
3. 任何产品标记“已量产/已出货”时必须附公司 A1/A2 依据，明确产品名和时间；
4. `pitch`、`W2W/D2W/C2W`、客户、良率、产能、收入缺少原文时直接留空；
5. 任何市场份额、CAGR、die/wafer/package/stack 数必须另建模型，并显著标为 A6 情景，禁止作为实际数据。
