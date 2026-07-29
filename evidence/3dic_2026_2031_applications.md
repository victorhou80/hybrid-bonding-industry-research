# Run B｜2026–2031年3D IC应用、渗透与客户起量研究

**角色：应用与渗透研究组｜资料截点：2026-07-29｜初稿，供监工与其他组质询**

> 本组回答的是“3D IC商业机会会在哪些应用、以什么节奏出现”，不是把所有带“3D”“stacked”“chiplet”字样的市场收入相加。报告严格拆分：HBM attached 2.5D/3D系统、logic-on-cache/logic direct 3D、CIS、3D NAND、非HBM chiplet、移动/边缘、汽车、CPO/光子、MEMS/RF、量子/科研。任何百分比均为本组A6情景带，除非明确标为公司披露；不代表厂商订单、行业统计或实际单位出货。

## 1. 结论先行

1. **2026–2028的收入增长中心仍是AI/HPC的“HBM + 大尺寸2.5D/3D系统封装”，但它不等于hybrid bonding。** HBM4的标准、客户认证、base die、测试和系统平台同步决定起量；TSV+micro-bump/TCB与hybrid bonding会并存。
2. **direct 3D最强的可核验商业样板是CIS和AMD 3D V-Cache，而不是“所有AI芯片”。** CIS已成熟、单位增长趋稳但工艺价值量继续提高；logic-on-cache从高端CPU向更多服务器/客户端SKU扩散，绝对量仍缺公开账本。
3. **3D NAND是最大的垂直结构bit市场，却不能与先进封装收入合并。** 多deck、array–CMOS分离制造及晶圆键合的采用，取决于每bit成本和良率，不随CoWoS/HBM周期同步。
4. **2028–2031的第二增长曲线是定制XPU/chiplet、CPO和更深的logic/cache 3D。** CPO在2026–2027主要仍是平台验证、小批量与首代系统导入；若可维护性、光引擎良率和热问题解决，2028–2030才可能出现阶跃式收入。
5. **汽车、移动、MEMS/RF是“内容价值量机会”，不是短期direct-bond巨量机会。** 移动BOM极敏感；汽车资格周期长且要求十年以上供货；MEMS/RF结构与封装高度异质，很多产品是wafer-level packaging而非Cu–Cu hybrid bonding。
6. **量子/科研在2031年前主要贡献高毛利工程、设备、低温互连和小批量多项目，不贡献可审计的大宗die量。** 研究demo不得写成量产。

## 2. 状态审计：截至截点商业化走到哪一步

| 应用 | 典型结构 | 截点状态 | 可确认 | 严禁外推 |
|---|---|---|---|---|
| AI/HPC：HBM attached | GPU/XPU + HBM stack + interposer/RDL/bridge | **成熟出货并高速爬坡**（HBM3E/2.5D）；HBM4处于送样、认证、量产准备/初始导入的厂商差异阶段 | NVIDIA/AMD数据中心业务、HBM产品发布、CoWoS类平台存在 | HBM4=hybrid bonding；HBM收入÷假设ASP=stack数；CoWoS WPM=GPU数量 |
| AI/HPC：logic-on-cache | SRAM cache die直接堆在CPU logic上 | **成熟商业出货，但集中于命名SKU** | AMD Ryzen/EPYC 3D V-Cache与TSMC SoIC路线 | 全部AMD CPU、全部SoIC、所有3D V-Cache均有公开单位数或统一pitch |
| AI/HPC：logic-on-logic | compute/IO/base die垂直堆叠，direct bond或细间距互连 | **平台量产能力+选择性产品；更细pitch direct路线爬坡/验证** | SoIC、Foveros、Foveros Direct、X-Cube平台 | 平台发布=外部客户大批量；Foveros产品=Foveros Direct出货 |
| CIS | pixel wafer/die + logic/ISP层 | **最成熟的大规模堆叠商业应用之一** | Sony stacked CIS、Cu–Cu连接技术与双层晶体管像素路线 | Sony传感器总出货=hybrid-bonded出货；所有品牌stacked CIS均是Cu–Cu |
| 3D NAND | cell array多层；部分array与CMOS分离并bond | **大规模成熟出货；bonding架构按厂商/代际不同** | YMTC Xtacking、Kioxia CBA等公开架构 | CuA/4D/COPS/所有3D NAND自动等于W2W Cu–Cu hybrid bond |
| 非HBM CPU/GPU/chiplet | 2.5D bridge/RDL、3D base die、UCIe/专有die-to-die | **已量产，但开放多供应商chiplet仍在生态建设** | Foveros/EMIB/SoIC、UCIe规范和EDA 3D流 | UCIe合规=跨厂KGD、热、可靠性和责任边界已解决 |
| 移动/边缘 | PoP、fan-out、SiP、stacked CIS，少量3D logic机会 | **先进封装成熟；direct logic 3D仅旗舰/研发期权** | InFO/fan-out/PoP和stacked CIS已广泛商业化 | 手机出货总量并入3D IC/HBM；chip stacking字样自动算hybrid bonding |
| 汽车 | 域控SoC+存储/PMIC/RF SiP，未来chiplet | **SiP/FC-BGA成熟；高密度3D logic处于缓慢导入/验证** | OSAT车规封装与AEC-Q资格体系存在 | 数据中心产品通过后可直接移植车规；技术demo=车厂SOP |
| CPO / silicon photonics | switch/XPU + photonic IC + laser/optical engine，2.5D/3D/C2W | **验证、首代平台导入、小规模收入**；不同厂商进度差异大 | 领先芯片/代工/封装厂公开硅光与先进封装方向 | CPO发布=机柜大规模部署；光引擎收入=hybrid bond收入 |
| MEMS/RF | sensor/MEMS cap wafer、ASIC、RF front-end、WLP/TSV | **WLP/键合成熟；Cu–Cu direct bond仅部分结构** | MEMS/RF长期采用晶圆级封装与异质集成 | 所有wafer bonding都等于3D IC或hybrid bonding |
| 量子/科研 | 低温控制chip、量子die、interposer、TSV/超导互连 | **研发与小批量工程验证** | IEEE/imec/科研路线图显示异构与3D互连研究 | qubit数、论文或demo换算商业die量 |

## 3. 2026–2031逐年应用节奏

### 3.1 年度主叙事

| 年度 | AI/HPC—HBM系统 | direct logic/cache | CIS / NAND | CPO、汽车与其他 | 当年真正拐点 |
|---|---|---|---|---|---|
| **2026** | HBM3E仍主量；HBM4随下一代平台进入认证/初始爬坡，供应瓶颈从单一封装转为HBM+封装+基板+测试+热共同约束 | 3D V-Cache扩大商业SKU；3nm SoIC stacking进入TSMC所称volume production窗口；Foveros Direct关注外部design win而非平台声明 | CIS稳定迭代；NAND通过更高层数/多deck/分离架构改善bit成本 | CPO首代平台/小批量；汽车主要是传统SiP与高端域控资格验证 | HBM4是否与GPU/ASIC平台同季通过认证；direct 3D是否出现第二类高量产品 |
| **2027** | 定制ASIC与GPU并行带来需求阶跃；更多HBM容量/stack与更大封装增加系统价值量 | 高端CPU/AI逻辑–缓存导入扩大，仍集中高毛利SKU | stacked CIS进入更多高端像素/事件/工业需求；NAND路线由单纯堆层转向架构与bond组合 | CPO从demo转向具名交换平台；汽车chiplet仍以工程样片/定点为主 | 第二/第三HBM来源稳定交付；非TSMC先进封装连续两个季度量产迹象 |
| **2028** | HBM4/后续增强型成为高端平台主力之一；推理ASIC使需求从少数旗舰GPU向多客户分散 | direct 3D从cache向精选logic-on-logic/near-memory扩张的首个较可信窗口 | CIS增速低于AI但价值量上升；NAND bonding采用取决于每bit成本优势 | CPO若解决可维护性与热，进入明显起量；首批高算力车规异构封装项目可能SOP | “多客户、多产品周期、可复购”的设备/封装收入出现，而非单次demo |
| **2029** | 大封装面积、供电、冷却、网络成为比单一bond pitch更强约束；模块量增速开始下台阶，容量/价值量仍快增 | 更多chiplet/3D PDK、DFT与热签核成熟，D2W因KGD优势扩大 | NAND受存储周期影响波动；CIS在XR/机器人/工业感知获得结构性需求 | CPO进入竞争分化；汽车资格完成后按车型平台缓慢爬坡 | 开放chiplet是否出现跨厂、跨代稳定量产；CPO每端口TCO是否胜出 |
| **2030** | AI系统从“买芯片”转向总拥有成本优化，单位封装ASP可能被良率学习压低，但die/stack/测试内容增加 | direct 3D成为部分高端计算平台的常规选项，仍非所有产品默认 | 成熟CIS直接键合维持规模；NAND多路线并存 | 汽车/工业边缘是可靠性导向的第二梯队；MEMS/RF以异质SiP受益 | 3D设计/测试标准化能否显著缩短首颗芯片周期 |
| **2031** | 高端GPU/XPU多数继续依赖HBM类高密度系统集成；替代路线按成本/工作负载分层 | logic/cache direct 3D形成可辨识子市场，是否成为主流取决于良率、热和可测试性 | CIS保持成熟龙头；NAND仍是最大垂直bit市场但商业周期独立 | CPO若成功成为交换/scale-up网络重要选项；量子仍偏工程市场 | 行业从“先进能力稀缺”转向“合格产能、设计生态、系统TCO”的竞争 |

### 3.2 相对增长区间（A6情景，不是行业统计）

**定义：** 表中为“与该应用相关的3D/高密度异构集成商业价值量”同比区间；价值量包括相应高密度互连、封装、测试或bonding内容，不包括整机、整颗逻辑die和全部存储器收入。CPO/量子等小基数项目的高百分比不可与CIS/NAND的巨大基数横比。

| 应用价值量YoY | 2026 | 2027 | 2028 | 2029 | 2030 | 2031 | 六年判断 |
|---|---:|---:|---:|---:|---:|---:|---|
| **AI/HPC：HBM attached系统封装** | 35–55% | 25–40% | 20–35% | 15–28% | 12–22% | 8–18% | 模块量增速下台阶，但每模块HBM容量、封装面积和测试价值提高；与旧总报告5.6→15.8m模块的A6基准方向一致 |
| **logic-on-cache direct 3D** | 18–35% | 20–40% | 18–35% | 15–30% | 12–25% | 10–22% | 从较小基数扩SKU；AMD商业样板强，但单位账本缺失 |
| **logic-on-logic / near-memory direct 3D** | 10–30% | 20–45% | 25–50% | 20–40% | 15–35% | 12–30% | 2028前多为少数高端design win；若热/良率失败则落在下沿 |
| **stacked CIS相关3D价值量** | 5–12% | 5–12% | 4–10% | 4–10% | 3–9% | 3–9% | 成熟大基数；由高端像素、传感+logic分层、XR/机器视觉驱动，不靠“首次采用” |
| **3D NAND垂直/键合相关价值量** | -5–20% | 5–25% | 5–22% | -8–20% | 3–20% | 3–18% | 强周期性；bit增长、层数/多deck与设备强度上行，但ASP/CapEx周期可使当年价值量负增长 |
| **非HBM CPU/GPU/网络chiplet** | 12–25% | 15–30% | 15–30% | 12–25% | 10–22% | 8–20% | 由reticle、yield、产品复用驱动；UCIe与开放生态的兑现决定上沿 |
| **移动/边缘3D/异构封装内容** | 3–10% | 4–12% | 5–15% | 5–14% | 4–12% | 4–12% | 手机单位增速有限，机会来自每机封装内容和传感器堆叠；direct logic受BOM/热约束 |
| **汽车3D/异构封装内容** | 6–15% | 8–18% | 10–22% | 10–22% | 8–18% | 7–16% | 定点到SOP滞后2–4年；高算力域控与区域化供给驱动，可靠性把斜率拉平 |
| **CPO / silicon photonics 3D集成** | 20–60% | 30–80% | 40–100% | 30–70% | 20–50% | 15–40% | 极小基数、波动极大；2028前最关键是具名平台和连续采购，不是百分比本身 |
| **MEMS/RF异质/WLP** | 4–12% | 5–14% | 5–14% | 4–12% | 4–12% | 3–10% | 结构多样，不能把全部WLP列作3D IC；汽车、工业与可穿戴支撑稳健内容增长 |
| **量子/科研3D互连工程收入** | 15–50% | 15–50% | 15–45% | 12–40% | 10–35% | 10–30% | 小批多项目；设备、工程和IP比die量更有意义，基数变化可造成失真 |

### 3.3 “渗透率”应如何可审计地表达

公开资料缺少统一分子/分母，因此本组不虚构“2031占全部芯片X%”。使用三级区间：

| 应用 | 2026新设计采用程度 | 2031基准状态 | 触发上修 | 触发下修 |
|---|---|---|---|---|
| 高端训练XPU采用HBM+2.5D/3D | **高**（已为主流架构） | **很高**，但低成本推理/边缘有替代内存路线 | 多家ASIC、HBM4/5多供方、供电/冷却扩张 | AI CapEx回撤；推理转向低带宽/片上SRAM/分布式架构 |
| 高端CPU采用3D cache | **中等，命名SKU集中** | **中高**，按工作负载分层 | 服务器/客户端连续扩SKU且价差被客户接受 | SRAM cache成本、热或软件收益不达预期 |
| 高端逻辑采用direct logic-on-logic | **低** | **低至中** | 具名旗舰量产、第二产品周期、良率与热数据 | TCB/bridge/RDL性能足够且成本更低 |
| 高端CIS采用stacked sensor/logic | **高** | **很高/成熟** | XR、机器视觉、event sensing、片上AI | 手机摄像头规格放缓；高端功能不下沉 |
| 3D NAND采用分离array–CMOS bonding | **厂商/代际分化** | **中高但非全行业统一** | bond方案显著改善bit density、周期和良率 | 单晶圆CuA/COPS或其他架构成本更优 |
| CPO在高端交换/scale-up网络 | **低，验证/首代** | **低至中；上行情景可达中高** | 可插拔铜/光I/O功耗越界；可维护性与良率解决 | 可插拔光学继续降功耗/成本；laser/thermal/serviceability失败 |
| 汽车direct 3D logic | **极低** | **低** | 车规KGD、可追溯、冗余、安全标准形成 | qualification太长、成本/供应风险高、单片SoC足够 |

## 4. 各应用的客户需求、价值量与替代路线

### 4.1 AI/HPC：HBM与direct logic必须分开

**HBM系统需求。** 客户购买目标是token吞吐、训练时长、上下文容量、每瓦性能和机柜规模扩展，而不是单项bond pitch。高价值链包括HBM KGD、TSV stack、base die、大尺寸interposer/RDL/bridge、先进基板、组装、测试、lid/TIM/cold plate。随着每模块stack数、每stack容量、封装面积与测试时间增加，封装/测试价值量可快于模块单位增长。

**弹性。** 训练旗舰对HBM价格相对低弹性，平台延期的机会成本高；成本敏感推理弹性更高，可采用GDDR、LPDDR、片上SRAM、分层内存、较小模型或更高利用率软件。因此“AI token增长”不能线性变成HBM需求。

**direct logic/cache需求。** 3D cache主要解决片外/片间访存延迟和带宽；logic-on-logic进一步降低互连RC并突破reticle，但叠加热密度、KGD和不可返工损失。其ASP/价值量高于平面封装，但必须由性能/能效或整机TCO覆盖良率溢价。

**资格周期。** HBM与XPU协同通常跨样品、控制器/PHY、封装、板卡、系统可靠性和云规模验证，研究上按约12–24个月管理；全新direct 3D结构按18–36个月、且至少一个完整产品周期验证。此为工程经验区间，不是任何厂商承诺。

### 4.2 CIS：成熟规模市场，价值量由功能分层而非单位爆发驱动

客户需要更小像素、更高动态范围、更快readout、片上ISP/AI与更低功耗。stacked pixel/logic允许不同工艺节点分别优化，并支持双层晶体管像素等结构。手机单位趋稳意味着收入弹性转向高端摄像头数量、sensor面积、汽车/工业/XR和每颗logic含量。替代路线包括单片BSI与成熟stacked但非Cu–Cu互连；因此只能对命名结构核验。消费CIS资格通常约12–24个月，汽车/工业更长。

### 4.3 3D NAND：机会在bit成本与设备强度，不是AI封装ASP

需求来自企业SSD、客户端SSD、UFS与AI数据湖，但价格周期、库存和资本开支会使设备/晶圆价值量剧烈波动。多层cell、string stacking/multi-deck、CMOS位置优化和array–CMOS bonding共同竞争。bonding能让array与外围分别优化、缩短工艺循环或改善面积效率，但引入双晶圆良率、对准、界面和额外工序成本。产品资格按客户端/企业级约12–30个月管理；企业和车规更长。

### 4.4 chiplet、移动与边缘

chiplet的客户价值是把大die拆分以改善reticle/yield、复用IP并混合节点；开放生态还需要UCIe、跨厂PDK、KGD、security、热/PDN和责任归属。2026–2028更现实的是单厂或强协调下的封闭chiplet，2029后才观察跨厂开放生态是否真正量产。

移动端需要薄型、低功耗和低BOM；fan-out、PoP、SiP、stacked CIS早已成熟，但direct logic 3D只有在节能/面积收益大于良率和热成本时进入少数旗舰。边缘AI内存带宽需求低于数据中心，HBM并非默认答案。

### 4.5 汽车

客户先看功能安全、AEC-Q可靠性、失效可追溯、冗余、供应连续性和十年以上供货，再看互连密度。高算力域控、中央计算、雷达/视觉融合和区域控制提高异质封装内容，但新结构从样品、Tier-1/车厂验证到SOP可需24–48个月，车型平台爬坡又需数年。direct bond不可返工和热循环风险使汽车采用慢于数据中心；商业机会更早出现在先进测试、可靠性、SiP、基板与热材料。

### 4.6 CPO / photonics

CPO的驱动是交换带宽提升后，板级电I/O与可插拔光模块的功耗、距离和前面板密度压力。其3D IC机会包括electronics–photonic die C2W/D2W、interposer/RDL、laser attach、光纤耦合、热隔离和全链测试。价值量高，但良率是乘法：逻辑、光子、激光器、耦合与封装任一失效都可报废高价值组件。

客户资格需通过高温/寿命、光功率、误码、可维护性与系统软件，按18–36个月管理。最大替代是持续改进的可插拔光学、linear pluggable optics、铜缆和更低功耗SerDes。2028是本组基准情景的起量窗口，不是确定量产日。

### 4.7 MEMS/RF与量子

MEMS/RF常需要cap wafer、真空腔、TSV、sensor+ASIC堆叠或SiP，晶圆键合成熟但材料和界面不同；因此机会更多属于WLP、键合、测试、特种材料和定制设备，不应全算Cu–Cu hybrid bonding。RF前端还受到声学滤波、天线、III-V与CMOS异质材料约束。

量子计算需要低温控制、超导/硅自旋/光量子die与interposer的低损耗互连，3D有助于布线和I/O密度，却引入热负载、材料损耗、磁/射频串扰和低温可靠性。到2031商业机会更可能是研究晶圆、小批封装、低温探针/测试和共同开发，而非消费电子式出货。

## 5. 商业机会排序

| 优先级 | 2026–2028 | 2029–2031 | 为什么 |
|---|---|---|---|
| **第一梯队** | HBM KGD/测试、2.5D大封装、先进基板、热管理；CIS成熟链；3D NAND设备/工艺 | AI封装持续、direct logic/cache扩大、NAND按周期 | 有实物商业基础、客户痛点刚性；但三者口径不可相加 |
| **第二梯队** | 3D cache、定制ASIC/chiplet、EDA/3D PDK、量测/失效分析 | logic-on-logic、跨厂chiplet、CPO量产链 | 价值量高，qualification与生态决定斜率 |
| **第三梯队/期权** | CPO首代、汽车高密度异构验证、MEMS/RF定制bond | CPO扩张、汽车平台SOP、近存/边缘特殊架构 | TAM可观但技术路线与量产时间不确定 |
| **科研期权** | 量子/低温3D、晶圆级光学、专用传感 | 小批工程收入与IP许可 | 高毛利、小体量、不能用论文热度推销量 |

**最值得投资/经营跟踪的“卖铲子”环节：** KGD与高速测试、warpage/热/应力协同、hybrid bonding前清洗/CMP/量测、bond后无损检测、临时键合/薄化、基板/RDL、低温/光电测试、3D EDA与design kit。它们横跨多个应用且不押注单一客户；但工具订单仍不是下游出货。

## 6. 风险、反身性与领先指标

| 风险 | 影响应用 | 领先指标（应看什么） |
|---|---|---|
| AI CapEx/电力/液冷受限 | HBM、GPU/ASIC、CPO | 数据中心投运MW、机柜交付、客户平台GA，而非只看CapEx口号 |
| HBM4 qualification延期 | AI/HPC | 客户联合公告、volume shipment、XPU平台同时GA；不能只看样品 |
| 良率与不可返工损失 | direct logic、CPO、汽车 | 具名产品第二代、重复订单、保修/可靠性数据、封装毛利趋势 |
| TCB/RDL/bridge继续改进 | hybrid bonding | pitch/功耗收益是否足够覆盖direct bond成本；客户BOM选择 |
| NAND下行周期 | 3D NAND | 原厂库存、bit shipment、ASP、CapEx，而非层数新闻 |
| 手机规格降级 | CIS、移动封装 | 单机sensor面积/数量、高端机结构和汽车/工业占比 |
| 汽车平台延期 | 汽车 | design win不等于SOP；需看车型量产、PPAP/AEC-Q和长期供货协议 |
| 标准碎片化/IP责任 | chiplet | UCIe互操作、跨厂reference flow、KGD责任和安全认证 |
| 出口管制/区域化 | 中国与全球供应链 | 设备交付、维护耗材、EDA许可、HBM可获得性和替代路线实际良率 |

## 7. 证据等级与来源台账（至少20条）

**等级：** A1=财报/监管/实际收入；A2=公司产品、量产或正式发布；A3=标准组织/官方资格体系；A4=技术平台/白皮书/路线图；A5=署名行业新闻；A6=本组情景推演。A2的“量产准备/送样”不能升级为A1实际出货。

1. TSMC 3DFabric（CoWoS/SoIC/InFO平台）：https://www.tsmc.com/english/dedicatedFoundry/technology/3DFabric —— **A2/A4**。
2. TSMC SoIC（W2W/C2W、bond pitch与代际）：https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/SoIC.htm —— **A2/A4**。
3. TSMC HPC/3DFabric（大封装路线）：https://www.tsmc.com/english/dedicatedFoundry/technology/platform_HPC_tech_WLSI —— **A2/A4**。
4. TSMC 2025 Technology Symposium：https://pr.tsmc.com/english/news/3122 —— **A2**。
5. AMD 3D Chiplet技术入口：https://www.amd.com/en/corporate/events/3d-chiplet.html —— **A2/A4**。
6. AMD Ryzen 7 5800X3D商业发布：https://www.amd.com/en/newsroom/press-releases/2022-3-15-amd-unveils-world-s-fastest-gaming-desktop-proce.html —— **A2**。
7. AMD EPYC Milan-X商业发布：https://www.amd.com/en/newsroom/press-releases/2022-3-21-amd-epyc-processors-with-amd-3d-v-cache-technol.html —— **A2**。
8. AMD 2024全年财报：https://ir.amd.com/news-events/press-releases/detail/1228/amd-reports-fourth-quarter-and-full-year-2024-financial-results —— **A1**，只能证明业务收入，不直接证明3D封装单位。
9. AMD MI350/MI400路线：https://www.amd.com/en/newsroom/press-releases/2025-6-12-amd-unveils-next-gen-rack-scale-ai-infrastructure-.html —— **A2**。
10. Intel Foveros：https://www.intel.com/content/www/us/en/architecture-and-technology/foveros.html —— **A2/A4**。
11. Intel Foundry先进封装：https://www.intel.com/content/www/us/en/foundry/advanced-packaging.html —— **A2/A4**。
12. Intel Foundry Direct Connect 2025：https://newsroom.intel.com/intel-foundry/intel-foundry-gathers-customers-partners-outlines-priorities —— **A2**。
13. Samsung Foundry advanced packaging：https://semiconductor.samsung.com/foundry/advanced-packaging/ —— **A2/A4**。
14. JEDEC HBM4标准发布：https://www.jedec.org/news/pressreleases/jedec-announces-publication-hbm4-standard —— **A3**，标准存在不证明任一厂商出货。
15. Micron HBM4送样：https://investors.micron.com/news-releases/news-release-details/micron-ships-hbm4-key-customers-power-next-gen-ai-platforms —— **A2（送样）**。
16. SK hynix HBM4开发完成/量产准备：https://news.skhynix.com/en/sk-hynix-completes-worlds-first-hbm4-development-and-readies-mass-production/ —— **A2（公司状态）**。
17. NVIDIA FY2025财报：https://nvidianews.nvidia.com/news/nvidia-announces-financial-results-for-fourth-quarter-and-fiscal-2025 —— **A1**，收入不反推模块/HBM数。
18. Sony stacked CMOS image sensor：https://www.sony-semicon.com/en/technology/mobile/stacked-cmos.html —— **A2/A4**。
19. Sony双层晶体管像素stacked CIS：https://www.sony-semicon.com/en/info/2021/202112/20211215.html —— **A2/A4**。
20. Samsung ISOCELL产品入口：https://semiconductor.samsung.com/image-sensor/ —— **A2**；不能据“stacked”判定Cu–Cu。
21. YMTC Xtacking：https://www.ymtc.com/en/technology/xtacking —— **A2/A4**；证明array/periphery分离与bonding路线，不自动证明每代Cu–Cu细节。
22. Kioxia CBA/BiCS产品发布：https://www.kioxia.com/en-jp/business/news/2020/20201020-1.html —— **A2**。
23. Samsung V-NAND/COPS：https://semiconductor.samsung.com/newsroom/tech-blog/the-technology-behind-samsungs-8th-generation-v-nand/ —— **A2/A4**；COPS不等于hybrid bond。
24. UCIe Specification：https://www.uciexpress.org/ucie-specification —— **A3**；互连标准不等于开放chiplet量产生态。
25. IEEE Heterogeneous Integration Roadmap：https://eps.ieee.org/technology/heterogeneous-integration-roadmap.html —— **A4**。
26. Cadence Integrity 3D-IC：https://www.cadence.com/en_US/home/company/newsroom/press-releases/pr/2024/cadence-announces-integrity-3d-ic-platform.html —— **A2/A4**。
27. Ansys RedHawk-SC Electrothermal：https://www.ansys.com/news-center/press-releases/03-18-24-ansys-redhawk-sc-electrothermal —— **A2/A4**。
28. Amkor Arizona先进封装/测试项目：https://ir.amkor.com/news-events/news-releases/news-release-details/2024/Amkor-to-Build-Advanced-Semiconductor-Packaging-and-Test-Campus-in-Arizona/default.aspx —— **A2/A3（建设项目）**，不等于可售产能。
29. Automotive Electronics Council文档入口：https://www.aecouncil.com/AECDocuments.html —— **A3**，用于车规qualification要求，不证明3D IC采用率。
30. SEMI Advanced Packaging：https://www.semi.org/en/advanced-packaging —— **A4/A5入口**。
31. Xperi/Adeia DBI技术：https://www.xperi.com/technology/dbi/ —— **A4/IP方资料**。
32. EVG hybrid bonding：https://www.evgroup.com/technologies/hybrid-bonding/ —— **A2/A4（设备/工艺能力）**。
33. Besi hybrid bonding：https://www.besi.com/products/hybrid-bonding/ —— **A2/A4（设备）**。
34. KLA advanced packaging量测：https://www.kla.com/advanced-packaging —— **A2/A4**。
35. BIS先进半导体出口管制：https://www.bis.gov/press-release/commerce-strengthens-export-controls-restrict-chinas-capability-produce-advanced-semiconductors —— **A1/A3（监管）**。

## 8. 给总报告和监工的可直接引用结论

- 2026–2031不能用一个CAGR概括3D IC：AI/HBM系统价值最快且最可见；CIS成熟稳定；NAND强周期；direct logic/cache小基数高增长；CPO高期权；汽车慢资格；量子是工程市场。
- 年度基准节奏是：**2026 HBM4认证与SoIC代际窗口；2027 ASIC/多供应来源；2028 direct logic和CPO首个可信放量窗；2029跨厂chiplet与系统TCO验证；2030设计/测试标准化；2031按应用形成成熟、成长和期权三层市场。**
- HBM与hybrid bonding必须双轨记账：HBM stack可采用TSV+TCB/micro-bump，direct bond是否采用要逐厂商、逐产品、逐代核验。
- 量化时优先报告“同比情景带+触发器”，拒绝用总厂WPM、设备订单、整机收入或云CapEx填补缺失出货。
- 商业机会不只在bond tool：KGD/测试、CMP/清洗/量测、薄化、热/warpage、基板/RDL、EDA/3D PDK和系统qualification往往决定最终可售产能。

## 9. 本组自我质询点（供30轮debate）

1. AI/HBM价值量区间是否重复计入HBM本体、封装和逻辑die？本稿明确定义只含相关高密度互连/封装/测试内容。
2. 旧总报告的模块模型是否误作事实？本稿仅引用其方向，并持续标A6、误差至少±25–40%。
3. CIS成熟是否代表hybrid bond单位已知？否；没有逐型号BOM不得换算。
4. NAND负增长区间是否合理？价值量受库存/ASP/CapEx周期影响，可与bit shipment正增长并存。
5. CPO高百分比是否夸大？小基数造成高波动，须用具名客户、连续采购与系统部署验证。
6. 汽车是否应给2031高渗透？不应；本稿将direct 3D定位低渗透，把机会放在可靠性、测试和异质SiP。

---

**浏览限制披露：** 本轮按用户要求尝试连接Codex内置浏览器，但子任务环境返回 `Browser is not available: iab`；未使用桌面Chrome。本稿新增框架主要建立在现有仓库已核验的一手资料台账上，凡无法在本轮重新打开的页面均不提升证据等级；CPO、MEMS/RF、量子等增量场景只给条件式A6情景，不声称实际单位出货。
