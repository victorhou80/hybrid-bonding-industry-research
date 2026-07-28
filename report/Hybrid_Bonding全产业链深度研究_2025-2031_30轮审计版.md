# Hybrid Bonding（混合键合）全产业链深度研究：2025–2031

**资料截点：2026-07-28｜五组研究、30条交叉质询、监工审计版｜实际出货优先**

> **结论先行：** Hybrid bonding 不是一台键合机、不是普通3D封装的同义词，也不是HBM的另一种叫法。它是一条从晶圆设计、Cu/介质表面、CMP、清洗活化、亚微米对准、W2W或D2W直接键合、薄化、检测、KGD、可靠性到系统认证的完整制造体系。当前商业成熟度最高的是堆叠CIS；部分array–CMOS分离的3D NAND已实现巨大规模，但每一代是否属于Cu–Cu hybrid bonding仍须逐产品核验；逻辑领域最强的公开商用实证之一是AMD 3D V-Cache与TSMC SoIC；HBM、CPO和更多logic-on-logic是未来最大增量方向，却不能提前计入实际hybrid-bonded出货。

## 1. 定义、分类与容易犯的四个错误

混合键合通常指平坦化后的介质表面先发生直接键合，随后通过退火/热处理形成Cu–Cu电连接；它同时依赖介质—介质和铜—铜界面。根据组装对象可分：

| 路线 | 对象 | 优点 | 局限 | 典型适用场景 |
|---|---|---|---|---|
| W2W | 完整晶圆对完整晶圆 | 高吞吐、整片对准、适合上下层die阵列高度匹配 | 坏区相乘、die尺寸/排布约束强、不可挑KGD | CIS、部分array–CMOS NAND、多晶圆同构结构 |
| D2W/C2W | 已切割或挑选die对目标晶圆 | 可选KGD、异尺寸/异节点/异功能集成 | die搬运慢、对准与污染控制更难、成本高 | logic-on-cache、异构chiplet、光电集成 |
| W2D/D2D | 晶圆与die或die对die的其他变体 | 灵活 | 吞吐、夹持和量测复杂 | 小批异构、特殊封装 |

四个红线：

1. **TSV堆叠不自动等于hybrid bonding。** TSV是穿硅结构，层间仍可能是micro-bump/TCB。
2. **“stacked”或“direct bonded”不自动等于Cu–Cu hybrid bonding。** 必须查看介质和导体界面。
3. **HBM不等于hybrid bonding。** HBM是DRAM产品/接口/stack体系；大量HBM仍用TSV+TCB/micro-bump。
4. **CoWoS、Foveros、X-Cube、2.5D封装不应整个平台打包计入。** 必须定位到产品、版本和键合界面。

## 2. 商业化成熟度：实际发生在哪里

| 应用 | 2026状态 | 已证实代表 | 真实驱动 | 2025–31趋势 | 最易夸大的地方 |
|---|---|---|---|---|---|
| 堆叠CIS | **最成熟的高量商业应用** | Sony堆叠CIS/双层晶体管像素；其他CIS需逐型号确认 | 像素层与逻辑分别优化、面积、噪声、HDR、速度 | 成熟渗透，向更多像素/逻辑层和高端感知扩展 | 用Sony总CIS出货代替Cu–Cu器件数 |
| 3D NAND array–periphery | **大规模商业化，但工艺名称要逐代确认** | YMTC Xtacking、Kioxia CBA；Micron CuA/SK hynix 4D/Samsung COPS不能因名称自动算Cu–Cu | 阵列与外围分开优化、bit density、周期和成本 | 分离制造/键合架构扩大；成本与yield决定份额 | 把所有3D NAND都算hybrid bonding；把CuA误作Cu–Cu |
| logic-on-cache | **已有明确商用产品** | AMD Ryzen/EPYC 3D V-Cache + TSMC SoIC | 大缓存、低延迟、低互连能耗，不必整体缩节点 | 从缓存向更多逻辑分区扩展，仍为高价值选择性市场 | 用AMD CPU收入反推SoIC die数量 |
| logic-on-logic | 平台量产开始、产品级透明度低 | TSMC SoIC；Intel Foveros Direct、Samsung X-Cube须逐产品核验 | reticle限制、异节点、PPA、IP复用 | 2027后若多客户量产与良率闭环，可能成为最大价值增量 | 把平台存在当全部产品出货 |
| HBM/3D DRAM | 当前HBM大多仍是TSV+TCB/micro-bump；HB方向处于逐代评估 | 三大DRAM厂HBM路线；没有统一一手材料支持HBM4全面切换 | stack高度、pitch、功耗、I/O和热 | 16-high/HBM4E或更后代可能成为采用窗口，但路线可能推迟 | HBM4=hybrid bonding，12-high=direct bond |
| Photonics/CPO | 高潜力、资格期长 | TSMC COUPE/SoIC路线、foundry/光子生态平台 | 电子—光子短互连、带宽密度、封装尺寸 | 2027–31先在高价值系统选择性导入 | 把实验器件/平台算系统出货 |
| MEMS/传感 | 小型化、腔体和可靠性驱动的稳定市场 | 各晶圆级封装平台，需逐产品确认导体界面 | wafer-level sealing、尺寸、可靠性 | 温和渗透 | 把氧化物/熔融键合全算Cu–Cu |

### 最强的量产实证序列

公开材料所支持的合理排序是：

```text
CIS直接互连成熟量产
        ↓
部分3D NAND的array–CMOS分离/晶圆键合规模化
        ↓
AMD 3D V-Cache等logic-on-cache商用
        ↓
更多logic-on-logic、多层memory-on-logic选择性量产
        ↓
HBM/CPO/开放chiplet中的更广泛采用
```

这一排序是证据成熟度，不是市场收入或单位大小排序。

## 3. 完整产业链：从IP到系统客户

| 层级 | 关键任务 | 全球参与者例示 | 中国大陆参与者例示 | 决胜指标 |
|---|---|---|---|---|
| 基础IP/许可 | DBI/hybrid bonding专利、接口与集成IP | Adeia/Xperi DBI、TSMC/Intel/Samsung自有IP | 高校/研究院、制造与设备厂专利池 | FTO、授权费、工艺覆盖、客户可迁移性 |
| 3D设计/EDA | partition、floorplan、热/PDN/应力、DRC/LVS、DFT | Synopsys、Cadence、Siemens EDA、Ansys | 华大九天、概伦电子、芯和等 | 3D PDK、sign-off相关性、模型/实测闭环 |
| 功能晶圆设计 | logic、CIS pixel、SRAM、DRAM、NAND、photonics | AMD/NVIDIA/Apple等设计客户；Sony、存储原厂 | 算苗、兆易等候选设计方，关系逐项核验 | pad阵列、冗余、KGD、热预算、测试可达性 |
| 晶圆制造/3D平台 | 上下晶圆制程、TSV、hybrid bond集成 | TSMC SoIC、Intel Foundry、Samsung、Sony、YMTC、Kioxia | 新芯股份/XMC、长江存储；中芯/华虹/长鑫需特定产品证据 | 产品级量产、良率、客户、有效WPM |
| CMP/平坦化 | Cu/介质平坦、recess/dishing、roughness | Applied、Ebara、荏原、Lapmaster及材料生态 | 华海清科 | 纳米级全局/局部平坦度、缺陷、wafer bow |
| 清洗/活化/湿法 | 颗粒/有机物/金属污染、氧化层控制、表面活化 | EVG、SUSS、Applied、Lam、TEL、SCREEN等 | 盛美上海、北方华创等 | particle density、queue time、表面能、残留 |
| Cu沉积/电镀/介质 | pad/TSV Cu、barrier/seed、介质 | Applied、Lam、TEL、Entegris、Merck等 | 盛美、北方华创、拓荆、中微及材料厂 | void、Cu纯度、应力、界面可靠性 |
| 对准与键合 | W2W、D2W/C2W、低温键合 | Besi、EVG、ASMPT、SUSS、Applied | 拓荆Dione/相关预处理布局 | overlay、UPH、颗粒、tool uptime、热预算 |
| 临时键合/解键合 | 超薄晶圆载体、背面加工 | EVG、SUSS、Brewer Science | 国内临时键合材料/装备生态 | TTV、翘曲、残胶、解键合损伤 |
| 减薄/切割 | 背磨、CMP、laser/saw、die singulation | DISCO、ACCRETECH | 华海清科及国内减薄/划切生态 | 厚度、TTV、edge chipping、薄片破损 |
| 量测/检查 | surface、CD、overlay、void、buried defect | KLA、Onto、Camtek、Nova | 中科飞测、精测电子 | 漏检/误报、缺陷—yield相关性、inline闭环 |
| 测试/KGD | wafer sort、TSV continuity、BER、burn-in、SLT | Advantest、Teradyne、Cohu | 长川科技、华峰测控、OSAT内部平台 | 测试覆盖、秒数、并测、早期筛坏、失效定位 |
| OSAT/后段 | RDL、基板、封装、热、系统测试 | ASE、Amkor、JCET等 | 长电、通富、华天、盛合晶微 | direct-bond产品资格，而非先进封装总收入 |
| 材料/基板/热 | slurry/pad/chemicals/ABF/TIM/lid/cold plate | Entegris、Fujimi、Merck、Ajinomoto等 | 安集、鼎龙、上海新阳、深南/兴森等 | 牌号、批次、客户认证、热/翘曲/可靠性 |
| 下游系统 | CPU/GPU/XPU、手机、SSD、云、光通信、汽车 | 云厂、OEM、模型公司、手机/相机客户 | 国内AI/手机/存储/智算中心客户 | 性能/功耗/TCO、供应连续性、客户验收 |

### OSAT的正确位置

Hybrid bonding把一部分传统“后段”工作前移到wafer fab或foundry-like洁净工艺。TSMC、Sony、存储IDM拥有前后道协同优势；OSAT的机会在D2W组装、RDL/基板、测试、热与开放客户服务，但并不是所有OSAT先进封装收入都来自hybrid bonding。OSAT需证明的是具体direct-bond产品、工具/流程、客户qualification和稳定yield，而不是展示2.5D/3D能力图。

## 4. 主要玩家、产品roadmap与下一代转折点

| 玩家 | 当前可核验位置 | 路线/roadmap | 下一代转折点 | 不能外推 |
|---|---|---|---|---|
| TSMC | SoIC-X支持chip-on-wafer与wafer-on-wafer；sub-10µm规则；官网称3nm stacking于2025进入量产 | SoIC Gen-2兼容N2及以后，结合CoWoS/SoW、COUPE | 多客户3nm/N2产品收入、pitch缩小同时yield/成本稳定 | TSMC总先进封装/CoWoS产能=SoIC产能 |
| AMD | 多代Ryzen/EPYC X3D可售 | 3D V-Cache持续扩展；产品结构可演进 | 从缓存堆叠向更多逻辑/存储分区与多代复用 | CPU收入=hybrid bond出货 |
| Sony | 堆叠CIS和双层晶体管像素技术成熟 | 更复杂像素—晶体管—逻辑分层 | 新层数/功能以可售sensor和客户终端验证 | Sony CIS总量=Cu–Cu总量 |
| YMTC | Xtacking为商业NAND平台 | 阵列与外围分离制造持续迭代 | 更高层数、cycle time、bond yield和成本竞争 | Xtacking全部代际必然同一Cu–Cu工艺 |
| Kioxia | CBA为BiCS路线之一 | CMOS directly bonded to array | 新代CBA产品和bit成本/良率 | “directly bonded”自动等于指定Cu–Cu机制 |
| Intel | Foveros已商用；Foveros Direct为更细pitch直接键合路线 | Foundry advanced packaging外部客户化 | 首个具名可售Foveros Direct产品、稳定客户量产 | Meteor Lake/Lakefield都算Foveros Direct |
| Samsung | X-Cube及先进封装平台存在 | 3D IC与HBM/CPO协同 | 具名产品+Cu–Cu界面+量产闭环 | X-Cube/I-Cube/H-Cube全部算HB |
| HBM三大原厂 | HBM已规模商业化，hybrid bonding采用时间仍在变化 | TCB/micro-bump继续优化，同时研发HB | 16-high/HBM4E以后，HB在成本、良率、热和stack高度上胜出 | HBM4或12-high自动等于HB |
| Besi | 设备订单/收入提供最强设备侧商业信号之一 | D2W高精度/吞吐、与Applied合作生态 | 多客户复购、工具验收、hybrid bond收入/订单可持续 | 订单除ASP反推工具和die |
| EVG/SUSS/ASMPT/Applied | 覆盖W2W/D2W、清洗活化、临时键合和先进封装 | 集成式工艺单元、低温、inline量测 | 客户量产工具复购和OEE/yield | 产品页=实际客户产能 |
| 中国设备链 | 拓荆、华海清科、盛美等具有关键模块公开能力 | 从客户验证到完整工艺闭环 | 具名产品/客户、批量复购、yield和可靠性 | 国产化布局=规模替代 |

## 5. 实际订单、出货、产能和扩产：公开数据的边界

### 可用的硬数据

- Besi FY2025公开收入约`€591.3m`、订单约`€685.0m`、Q4订单约`€250.4m`。这是公司/设备侧实际商业数据；订单解释包含先进封装、2.5D、光子及hybrid-bond需求，但不能全部归入hybrid bonding。
- TSMC官网明确SoIC从sub-10µm bond-pitch规则起步，并称3nm stacking technology于2025进入volume production。这是平台/工艺量产状态，不是产品数量或有效WPM。
- AMD 3D V-Cache多代产品正式上市，是实际产品商业化证据；AMD不拆分相关单位、收入、SoIC die或良率。
- Sony堆叠CIS、YMTC Xtacking NAND为实际产品平台，但厂商不按键合工艺拆分单位/收入。
- 中国链可核验的是上市公司收入、产品/客户验证/量产措辞和新芯股份的三维集成平台；目前没有同口径W2W/D2W有效产能和hybrid-bonded die实际出货。

### 不能填的产能

全球几乎没有统一公开的：

- W2W hybrid-bond wafer/month；
- D2W good die/hour × utilization × yield后的有效产能；
- 按产品拆分的bonded wafer/die/package；
- 客户工具数量与实际OEE；
- Cu–Cu界面良率、void/overlay分布和返工损失。

因此本报告不拿全厂WPM、SoIC/CoWoS总产能、CapEx、设备订单、厂房面积或公司总收入反推hybrid bonding产能。

### 产能爬坡周期

```text
工具交付/安装
  → 单机验收和recipe开发
  → CMP/清洗/材料/计量闭环
  → wafer/die产品资格
  → 可靠性、测试和客户认证
  → yield/OEE爬坡
  → 实际可售产品交付
```

从设备交付到稳定产品通常跨多个季度，复杂多层结构可能跨1–2个产品周期。这个范围是行业经验，不是任何厂商的确定指引。

## 6. 核心技术与商业难点

1. **平坦度、Cu recess与颗粒。** 超细pitch直接键合没有焊料自对准和高度补偿；局部dishing、oxide topography或单颗粒即可形成void/open。
2. **overlay与wafer distortion。** 名义对准精度不等于全片、多层、薄化后的实际overlay；热处理和应力会放大边缘误差。
3. **W2W良率乘法。** W2W吞吐高，但上下晶圆坏区叠加；die尺寸或map不匹配会浪费好die。
4. **D2W吞吐和洁净度。** KGD提高组合良率，却引入切割、搬运、临时载体、逐die对准和更长queue time。
5. **不可返修和测试。** 键合后发现底层die/TSV/界面失效往往代价极高；测试必须尽可能前移，同时仍要覆盖隐藏界面。
6. **热与供电。** 互连能耗下降不代表系统热下降；logic-on-logic/memory提高局部热密度和垂直热阻。
7. **可靠性。** Cu扩散/氧化、介质裂纹、界面空洞、EM/TDDB、热循环、湿热和机械应力均需产品级认证。
8. **EDA/责任边界。** 多代工/多节点chiplet需要3D PDK、热/PDN/应力、DFT、IP保密和失效归责。
9. **成本。** 省掉bump/underfill不一定降低总成本；CMP、清洗、计量、KGD和报废可能吞掉互连收益。
10. **IP许可与生态锁定。** DBI/工艺专利、foundry PDK、设备recipe和客户认证共同形成切换成本。

### W2W还是D2W：经济性判断

| 条件 | 更偏W2W | 更偏D2W/C2W |
|---|---|---|
| 上下die尺寸/阵列 | 高度匹配 | 异尺寸、异节点、异功能 |
| 单die良率 | 高且均匀 | 昂贵die、需挑KGD |
| 产量 | 极高、稳定产品 | 高价值、产品组合多 |
| 工艺目标 | 吞吐和整片一致性 | 组合良率和设计灵活性 |
| 风险 | 坏区相乘、整片报废 | 搬运/颗粒/吞吐/成本 |

## 7. 竞争格局与主要玩家表现

这个市场不存在一张有意义的“综合份额表”，应按层级比较：

- **产品/制造平台：** Sony在CIS商业实证最强；TSMC在高端逻辑3D平台和客户生态领先；YMTC/Kioxia在array–periphery分离NAND具有差异化；Intel、Samsung拥有平台和纵向整合，但公开的direct-bond产品闭环少于平台宣传。
- **键合设备：** Besi在高精度D2W及设备商业信号上突出；EVG/SUSS强于W2W、表面处理、临时键合等系统；Applied以综合前道、CMP/表面工程和与Besi合作切入；ASMPT具广泛后段客户基础。
- **过程控制：** KLA/Onto/Camtek/Nova的检测量测决定能否在不可返修前筛坏；其价值常被低估。
- **材料：** 材料不是通用耗材，slurry、pad、clean chemistry、dielectric、carrier adhesive均需客户/recipe共认证，切换周期长。
- **OSAT：** ASE/Amkor/JCET等可受益于D2W、测试、RDL、基板和系统组装，但foundry/IDM占据核心界面时，价值边界需要重新谈判。
- **中国链：** 已形成设备材料和三维集成模块池；短板是公开可验证的具名量产产品、完整recipe、计量—yield闭环、客户复购和实际产能。

## 8. 中国大陆全产业链与真实状态

| 环节 | 代表参与者 | 当前可写事实 | 不能写 |
|---|---|---|---|
| 3D晶圆集成 | 新芯股份/XMC | 官网明确TSV、Hybrid Bonding、双/多晶圆堆叠、chip-to-wafer异构平台，并称有多年量产经验 | 算苗代工厂、具体Cu–Cu pitch、有效WPM/良率 |
| 3D NAND | 长江存储 | Xtacking商业产品/技术平台 | HBM或算苗DRAM供应商 |
| DRAM | 长鑫科技 | DDR/LPDDR产品与真实制造；兆易—长鑫2025实际DRAM采购代工11.82亿元 | HBM/Cu–Cu 3D DRAM/算苗供货 |
| 存储设计 | 兆易创新 | NOR/NAND/利基DRAM；与长鑫的真实代工链 | 160GB/16TB/s memory wafer供应 |
| 逻辑foundry | 中芯国际、华虹等 | 晶圆制造和特色工艺经营 | 未具名direct-bond工艺或算苗关系 |
| OSAT | 长电、通富、华天、盛合晶微 | 先进封装、TSV/2.5D/3D/测试布局；具体研发/量产逐家分级 | 泛先进封装=Cu–Cu量产 |
| 键合/表面设备 | 拓荆科技 | W2W/C2W相关产品与客户验证/产业化线索 | 工具数、客户名、A4E设备、有效产能 |
| CMP/减薄 | 华海清科 | CMP/减薄在集成电路、先进封装/3D IC场景应用 | 具体hybrid-bond产品良率 |
| 清洗/电镀 | 盛美上海 | 清洗、湿法、电镀实际设备业务 | 指定Cu–Cu客户或产能 |
| 刻蚀/沉积 | 北方华创、中微、拓荆 | TSV/薄膜相关模块产品和收入 | 单一项目全国产BOM |
| 检测量测 | 中科飞测、精测电子 | 缺陷、膜厚、CD/overlay等平台 | buried void/客户yield闭环（未披露） |
| 材料 | 安集、鼎龙、上海新阳等 | CMP/湿电子/封装材料业务 | 材料总收入=HB材料收入 |
| 测试 | 长川、华峰及OSAT | 测试设备/服务业务 | KGD、BER、stack yield（未披露） |
| EDA | 华大九天、概伦、芯和 | 相关设计/工艺/封装分析能力 | 指定3D PDK或客户sign-off（未披露） |
| 下游设计 | 算苗等 | 官网主张hybrid-bonding 3D TokenPU；8层/160GB/16TB/s按各自证据分级 | 指定供应商、已量产或实际销量 |

### 中国链的真正突破指标

不是“国产设备发布”，而是四个闭环同时出现：

1. 具名产品/客户与具体工具或材料；
2. 客户验收、批量复购或量产收入；
3. Cu recess、particle、overlay、void、yield和可靠性达到产品窗口；
4. 最终产品单位交付或收入确认。

## 9. Hybrid Bonding与HBM：共性、差异和路线判断

| 项目 | Hybrid Bonding | HBM |
|---|---|---|
| 性质 | 制造/互连工艺 | DRAM产品、接口与堆叠系统 |
| 可服务对象 | CIS、NAND、logic/cache、DRAM、photonics、MEMS | AI/HPC逻辑旁的高带宽内存 |
| 当前成熟路线 | W2W CIS/NAND、D2W logic-cache等 | TSV+TCB/micro-bump仍广泛量产 |
| 共同链 | TSV（适用时）、薄化、CMP、清洗、键合、检测、KGD、测试、热、EDA | 同左，并额外依赖DRAM die/base die/JEDEC接口 |
| HB特有难点 | 表面、overlay、不可返修、D2W吞吐 | DRAM良率、stack、宽I/O、refresh、HBM客户认证 |
| 关系 | 可能进入未来HBM的层间互连 | 不采用HB也仍可成为HBM |

2026年相关新闻甚至出现三大DRAM厂延后hybrid bonder、继续以TCB支持HBM4，以及把16-high HBM4E视为更早采用窗口的相反渠道判断。这恰好说明：**HBM4并不自动意味着hybrid bonding；采用时间取决于TCB继续缩pitch的能力、HB良率、热、stack高度和客户认证。**新闻只能作为A5路线信号，必须等待原厂产品/工艺公告。

## 10. 2025–2031渗透节奏与格局变化

| 时段 | 基准判断 | 转折验证 | 下行风险 |
|---|---|---|---|
| 2025–26 | CIS成熟；NAND键合架构扩大；SoIC/3D V-Cache证明逻辑商业性；HBM仍以传统堆叠为主 | TSMC 3nm SoIC量产、多代X3D、设备订单/复购 | 公开产能和产品单位仍不透明 |
| 2027–28 | logic/cache与高端异构设计选择性增加；更多foundry/OSAT平台客户资格 | 两个以上制造平台出现具名direct-bond量产客户；D2W吞吐/yield改善 | 成本、测试、不可返修使客户留在2.5D/TCB |
| 2029–31 | 若HB/多层逻辑/CPO通过资格，hybrid bonding从少数专用产品扩为重要平台选项 | HBM或CPO出现持续产品收入与稳定良率；开放3D PDK成熟 | TCB/micro-bump、RDL/bridge、单片集成继续足够好，HB停留高端利基 |

最可能的未来格局不是“hybrid bonding全面替代传统封装”，而是：

- CIS和部分NAND：W2W高量、IDM/专业制造平台主导；
- logic/cache：TSMC等foundry平台与高精度D2W设备生态主导；
- HBM：DRAM IDM根据代际和堆高在TCB与HB之间选择；
- CPO/MEMS：按系统/器件资格形成小而高价值的专用链；
- OSAT：从后段组装转向D2W、测试、RDL/热和客户服务差异化；
- 中国：设备模块国产化先行，真正份额提升取决于产品级量产闭环。

## 11. 算苗科技在完整产业链中的位置

算苗应被归为下游3D AI芯片设计/需求牵引者，而不是hybrid bonding设备、材料、晶圆制造或OSAT公司。公司/行业公开材料中的8层、160GB、16TB/s、TSV+bump、Hybrid Bonding和用户提供Cu–Cu线索必须分别标证据等级。

其潜在BOM会涉及定制存储晶圆、逻辑晶圆、TSV、CMP/清洗、W2W/D2W键合、薄化、检测、KGD、封装、测试、热和EDA；但目前没有任何具名存储厂、foundry、3D平台、OSAT、设备材料或客户公告。因此所有中国厂商只能列为能力候选，不能列为算苗供应商。

新增专利核验进一步强化但没有越过这条商业边界：中科声龙 `CN219040074U` 已在2022年申请文本中明确存储电路芯片—数据处理电路芯片的金属键合触点/Hybrid Bonding、DRAM访问与自检，但该专利2023年登记转让给 Shenglong (Singapore) Pte. Ltd.；算苗自己的 `CN121920305A` 权利要求直接写计算—存储芯片通过Hybrid Bonding互连，`CN121925162A`披露计算层—Buffer Die—存储层及TSV/HB、检测、冗余和多存储芯片堆叠。它们是A4级设计路线证据，不是A4E的Cu–Cu截面、8层量产、160GB/16TB/s实测或出货证据。两个申请主体及其专利资产不得因团队沿革而合并。

详见[中科声龙与算苗科技专利专项](中科声龙与算苗科技_3D存算及混合键合专利审计.md)。

真正转折点是封装截面/工艺说明、点亮与实测、客户验收、单位交付和收入，而不是流片、专利、融资或团队历史。

## 12. 数据质量、30轮审计与研究结论

五个研究组分别覆盖：A全球量产产品；B设备材料工艺；C中国全链；D商业产能；E竞争与roadmap。每组经过六轮监工质询，共30条。监工重点否决：

- stacked/TSV/2.5D平台自动算hybrid bonding；
- HBM4、Foveros、X-Cube、CoWoS整体计入actual shipment；
- 设备收入/订单换算bonded die；
- 总厂WPM/CapEx换算有效hybrid-bond产能；
- 中国工艺相关厂商自动成为算苗供应商；
- 技术论文/专利/样机升级为量产。

当前最可靠的商业判断是：hybrid bonding已经不是实验室技术，但它仍不是一个具统一统计口径的独立市场。实际产品渗透远高于公开“hybrid bonding收入/产能”的可见度。投资和产业研究应分别跟踪产品采用、制造平台、设备订单、材料认证与最终系统收入，不能用单一口径代替全链。

## 13. 核心一手来源

### 制造与产品

- [TSMC 3DFabric](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/3DFabric.htm)
- [TSMC SoIC](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/SoIC.htm)
- [AMD 3D Chiplet Technology](https://www.amd.com/en/corporate/events/3d-chiplet.html)
- [AMD Ryzen 7 5800X3D](https://www.amd.com/en/newsroom/press-releases/2022-3-15-amd-unveils-world-s-fastest-gaming-desktop-proce.html)
- [AMD EPYC with 3D V-Cache](https://www.amd.com/en/newsroom/press-releases/2022-3-21-amd-epyc-processors-with-amd-3d-v-cache-technol.html)
- [Sony 2-Layer Transistor Pixel](https://www.sony-semicon.com/en/technology/mobile/2-layer-pixel.html)
- [Sony 2021双层晶体管像素新闻](https://www.sony.com.cn/content/sonyportal/zh-cn/cms/newscenter/techonology/2021/20211217-1.html.html)
- [YMTC Xtacking](https://www.ymtc.com/en/technology/xtacking)
- [Kioxia BiCS FLASH](https://www.kioxia.com/en-jp/business/technology/bics-flash.html)
- [Intel Advanced Packaging](https://www.intel.com/content/www/us/en/foundry/advanced-packaging.html)
- [Samsung Advanced Packaging](https://semiconductor.samsung.com/foundry/advanced-packaging/)
- [新芯股份三维集成平台](https://www.xmcwh.com/site/3D-IC-platform)

### 设备、材料、测试与EDA

- [Besi 2025 Annual Report](https://www.besi.com/investor-relations/financial-reports-and-publications/financial-reports/)
- [EV Group](https://www.evgroup.com/)
- [SUSS Investor Relations](https://www.suss.com/en/investor-relations/news/)
- [ASMPT Financial Reports](https://www.asmpt.com/investor-relations/financial-reports/)
- [Applied Materials FY2024 Results](https://ir.appliedmaterials.com/news-releases/news-release-details/applied-materials-announces-fourth-quarter-and-fiscal-year-2024-results)
- [Lam Research FY2025 Results](https://newsroom.lamresearch.com/2025-07-30-Lam-Research-Corporation-Reports-Financial-Results-for-the-Quarter-Ended-June-29,-2025)
- [DISCO Financial Information](https://www.disco.co.jp/eg/ir/financial_information/)
- [KLA FY2025 Results](https://ir.kla.com/news-releases/news-release-details/kla-corporation-announces-fourth-quarter-and-fiscal-year-2025-results)
- [Advantest FY2024 Results](https://investor.advantest.com/en/ir/news/2025/20250425.html)
- [Adeia DBI Hybrid Bonding](https://adeia.com/semiconductor/inventing-connections-for-humanity)
- [Synopsys 3DIC Compiler](https://www.synopsys.com/implementation-and-signoff/3dic-compiler.html)
- [Cadence Integrity 3D-IC](https://www.cadence.com/en_US/home/tools/ic-package-design-and-analysis/integrity-3d-ic-platform.html)

### 中国链与法定披露

- [兆易创新2026年日常关联交易公告](https://static.cninfo.com.cn/finalpage/2026-03-31/1225061368.PDF)
- [长鑫产品](https://www.cxmt.com/product.html)
- [拓荆科技IR](https://www.piotech.cn/ir/)
- [华海清科](https://www.hwatsing.com/)
- [盛美上海IR](https://www.acmrcsh.com/investor-relations/)
- [北方华创财务报告](https://www.naura.com/EN/IR/FinancialReports/)
- [中微公司IR](https://www.amec-inc.com/en/ir/reports.html)
- [中科飞测](https://www.zkftech.com/)
- [长电科技IR](https://www.jcetglobal.com/investor/)

完整来源、公司逐项证据边界和原始五组研究见本项目`evidence/`与`debate/`目录。
