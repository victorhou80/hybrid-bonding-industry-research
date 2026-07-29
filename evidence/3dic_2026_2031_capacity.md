# Run C｜2026—2031年3D IC产能、CapEx、全链瓶颈与供需情景

**版本/信息截止日：** 2026-07-29
**研究职责：** 只研究供给侧：晶圆、2.5D/3D先进封装、HBM、W2W/D2W直接/混合键合、OSAT、设备、材料、基板、测试与散热的产能、扩产、建设周期、良率爬坡和供需松紧。
**重要限制：** 本稿是30轮debate的C组初稿，不是最终合稿。所有未由企业明确披露的2027—2031数字均标成“情景”，不能当作公司指引。

---

## 1. 执行结论

1. **2026—2031年3D IC不会有一个可加总的统一“WPM产能”。** CoWoS/2.5D中介层封装、SoIC/Foveros Direct式3D直接键合、传统Foveros微凸点、HBM堆叠、CIS W2W、NAND晶圆键合的工序、晶圆当量、die尺寸和良率完全不同。报告只能分别建账。
2. **截至2026-07-29，公开数据足以证明巨额扩产和真实设备收入，却不足以审计全球Hybrid Bonding有效WPM。** TSMC、Intel、Samsung、Sony、ASE、Amkor、JCET均未按客户、W2W/D2W、Cu–Cu工艺和稳定良率披露统一有效产能；“未披露”是正确答案，不应被媒体WPM填补。
3. **2026—2027最紧的不是一台键合机，而是AI封装全栈：先进逻辑wafer、CoWoS/RDL/interposer、HBM、ABF基板、临时键合/薄化、KGD测试、burn-in以及液冷/冷板。** 单点扩产会把瓶颈迁移，而不会消灭瓶颈。
4. **2028前后的供给拐点来自2024—2026开工的项目进入量产和认证。** Intel New Mexico Fab 9已经投产；Amkor Arizona按计划到本十年后段才形成美国本土先进封装；Micron Singapore HBM先进封装新厂计划自2026起逐步贡献；SK hynix M15X先于完整新fab扩出HBM供给。土建投产不等于客户可用产能，通常还需2—6个季度认证与良率爬坡。
5. **HBM4/4E/5将扩大3D IC商业机会，但不能把HBM产能写成Hybrid Bonding产能。** 2026—2028，TCB/micro-bump仍可能是主力量产路径；Cu–Cu是否进入某一代、某一堆叠高度，必须逐供应商、逐产品取得制造结构证据。
6. **2030—2031可能从“AI封装短缺”转向“合格产能结构性过剩与高端产能仍紧”并存。** 通用CoWoS/RDL或较旧HBM可能价格承压，但细间距D2W、超薄多层堆叠、HBM4E/5、光电共封装、先进测试和热设计仍有资格认证壁垒。
7. **设备商业机会的排序不是只看键合机。** 增量价值池依次扩散至CMP/平坦化、单晶圆清洗、表面活化、Cu沉积与电镀、临时键合/解键合、薄化/切割、亚微米对准、无损缺陷检测、pre-bond KGD、post-bond高速测试、热界面材料、冷板和基板。

---

## 2. 审计框架：必须分开的五本产能账

| 账本 | 正确物理对象 | 代表平台/玩家 | 可以从公开资料确认 | 不允许的换算 |
|---|---|---|---|---|
| 前道晶圆 | 300mm wafer starts、节点与产品组合 | TSMC、Intel、Samsung、Sony、三家DRAM厂 | fab/节点/总CapEx或项目投资（若公司披露） | 总WPM→3D IC有效产出 |
| 2.5D先进封装 | package、interposer/RDL面积、reticle倍数、HBM位数 | TSMC CoWoS、Samsung I-Cube、Intel EMIB、ASE/Amkor | 平台存在、扩产/厂房、部分第三方名义WPM | CoWoS WPM→SoIC/Hybrid Bonding WPM |
| 3D直接/混合键合 | bonded wafer pairs或bonded die，W2W/D2W分列 | TSMC SoIC、Intel Foveros Direct、Samsung X-Cube、Sony CIS | 平台、产品、设备订单；极少有效WPM | 键合机台数/总封装收入→有效产能 |
| HBM | good stacks、GB/bit output、堆叠高度与世代 | SK hynix、Samsung、Micron | 产品状态、公司收入/CapEx；少有标准化实物产能 | HBM bit增长→Hybrid Bonding产量 |
| OSAT与测试 | packages、die attach、test insertions、burn-in hours | ASE、Amkor、JCET、PTI、Advantest等 | 厂房投资、业务收入、平台能力 | OSAT总营收→3D IC出货 |

### 2.1 产能成熟度七级

```text
M0 公告/选址
 → M1 土建
 → M2 cleanroom与公用工程可用
 → M3 工具交付/安装
 → M4 工艺验收与材料/计量闭环
 → M5 客户qualification和可靠性通过
 → M6 稳定良率下的有效产能
 → M7 实际出货/收入
```

本稿只有企业明确报“量产/出货/收入”时才写M6/M7；项目投资只写M0—M3。一个厂房的总CapEx也不能拆成Hybrid Bonding专用CapEx，除非企业自己拆分。

---

## 3. 全球主要供给方：扩产、周期与公开产能边界

### 3.1 TSMC：CoWoS与SoIC必须拆分

| 项目 | 已确认事实 | 2026—2031供给含义 | 缺口/禁推 |
|---|---|---|---|
| CoWoS | TSMC将CoWoS列入3DFabric，面向logic+HBM等高性能系统；企业持续增加先进封装投资 | 2026—2028仍是AI GPU/ASIC系统封装的关键约束；扩产会拉动interposer/RDL、临时键合、基板和测试 | 第三方经常给出月产能，但晶圆当量、CoWoS-S/L/R结构和大封装面积不同。本稿不把媒体WPM写成审计事实 |
| SoIC | 官方明确支持W2W与CoW/D2W；3nm stacking technology于2025进入volume production，Gen-2面向N2以后 | 2026—2029高价值logic-on-cache、logic-on-logic及部分AI chiplet进入更多设计；对D2W对准、KGD、薄化和热测试需求高 | TSMC没有公开SoIC统一有效WPM、客户die数、稳定良率和收入；CoWoS扩产绝不等于SoIC扩产 |
| 先进封装基地 | 竹南AP6及后续台湾先进封装布局是供给扩展载体 | 新厂通常经历建设、装机、认证，名义开产后还需季度级爬坡；2026—2028投资对应本十年后段供给 | 厂房面积、总资本预算不能分解为SoIC或Cu–Cu专用产能 |

**CapEx口径：** TSMC FY2024资本预算与2025公司指引可以证明资本强度，但其资本预算主要投向先进制程，先进封装/测试/掩模只是公司披露区间中的一部分；不能将集团CapEx全部归入3D IC。2026以后使用年度公司指引滚动更新，不在本稿伪造2027—2031绝对数。

### 3.2 Intel：内生产品产能强，外部foundry利用率仍待验证

* Intel于2024年启用New Mexico Fab 9，官方披露投资约**35亿美元**，设施面积约400,000平方英尺，服务Foveros等先进3D封装。这是已建成实物资产（M4—M7按具体产品不同），不是Foveros Direct有效WPM披露。
* Foveros、Foveros Direct、EMIB要分账：Foveros商业产品可以使用micro-bump；Foveros Direct代表更细间距Cu–Cu直接互连；EMIB是2.5D桥接。Meteor Lake等产品出货不能自动计入Foveros Direct。
* 2026—2028的关键是Fab 9利用率、18A及外部foundry客户能否形成可复制的封装设计流；2029—2031若外部客户不足，物理能力与经济利用率可能显著背离。

### 3.3 Samsung：Foundry、先进封装和HBM同属集团，但不可合并产能

* X-Cube（3D）、I-Cube/H-Cube（2.5D/系统）和HBM是三个不同账本。Samsung公开平台与HBM产品路线，但没有统一披露X-Cube的W2W/D2W Cu–Cu有效WPM。
* Samsung的优势是逻辑、DRAM、base die、先进封装和终端协同；潜在瓶颈是HBM客户qualification、良率、热与封装工艺选择，而不是只有DRAM wafer starts。
* 2026—2027若HBM4客户认证改善，Cheonan等后段与DRAM前道投入会带动TCB/键合、测试和材料；若认证延后，设备安装可能先于收入，利用率压力增加。

### 3.4 Sony：CIS是最成熟的W2W/直接互连商业基盘

* Sony Semiconductor Solutions的堆叠式CMOS传感器及两层晶体管像素架构证明3D晶圆级集成已进入消费电子量产。
* Sony公开I&SS分部投资和收入，但没有将所有sensor wafer、特定Cu–Cu产品、W2W有效WPM分开披露。因此只能说“成熟大规模商业场景”，不能给Cu–Cu季度wafer数。
* 2026—2031增长来自高端手机多摄、汽车感知、工业/机器人、边缘AI传感器；风险是手机单位数成熟、客户集中、传感器尺寸扩大降低每片die数。机会集中在W2W键合、对准/缺陷检测、薄化和高可靠车规测试。

### 3.5 三家HBM厂：实际投入可确认，Hybrid Bonding采用不可外推

| 厂商 | 扩产/产品事实 | 投产与爬坡 | 2026—2031判断 |
|---|---|---|---|
| SK hynix | 官方公布M15X投资，项目总投入（含长期设备）约**20万亿韩元**，以较快扩大HBM供给；公司发布HBM4开发/量产准备状态 | fab建筑和设备分批投入；good stack还需DRAM die、base die、TSV/TCB、测试与客户认证共同爬坡 | 2026—2027供给领先优势取决于good stack而非裸DRAM wafer；HBM4/4E键合路线须逐产品确认 |
| Micron | 新加坡HBM先进封装厂官方规划投资约**70亿美元**至本十年后段，预计2026开始生产并逐步爬坡；这是后段封装投资，不是DRAM前道全部能力 | 2026初始产能到2028成熟之间存在安装、人员、客户和良率曲线 | 美国/新加坡双区域制造提高韧性；测试、TCB/键合、薄化与洁净度形成配套机会 |
| Samsung | HBM产品线和韩国DRAM/后段投资持续推进 | 客户qualification可能比工具安装更慢；产品世代切换造成旧线改造/新线并行 | 上行情景是HBM4大客户认证后快速释放垂直整合能力；下行情景是高CapEx而有效利用率滞后 |

**严格边界：** HBM出货主要以stack/GB/bit计，Hybrid Bonding设备以die/hour或wafer/hour计，两者不能在没有BOM、堆叠高度、良率与键合结构时相互换算。HBM4的2048-bit接口、logic base die和更高堆叠价值提高Cu–Cu的经济吸引力，但不等于全行业已经切换。

### 3.6 OSAT：扩产给3D IC“可外包性”，但最先进direct bond仍由IDM/foundry主导

| 玩家/项目 | 已确认事实与状态 | 周期/瓶颈 | 商业机会 |
|---|---|---|---|
| Amkor Arizona | 官方宣布美国先进封装测试基地，初始投资约**20亿美元**；美国商务部CHIPS奖励约**4.07亿美元**直接资助；按项目披露，量产目标在本十年后段 | 选址/土建→设备→客户qualification，约跨多年；客户产品在美国前道与后段协同是关键 | 2028—2031美国AI/HPC、汽车、国防可信供应链；基板、测试、热和本地工程服务 |
| Amkor Vietnam | 官方长期投资计划约**16亿美元**，初期投入约5.2亿美元，面向SiP与先进封装 | 新团队、良率和客户迁移爬坡；不是Cu–Cu专用工厂 | 亚洲供应链多元化、消费/通信/汽车先进封装 |
| ASE | 持续在高雄、马来西亚等地扩先进封装和测试；企业财报可确认真实收入/CapEx | AI package面积增大、HBM数量增加使测试时间、基板和热成为限制 | VIPack、2.5D/3D、硅光与系统级测试；但总CapEx不能换算Hybrid Bonding WPM |
| JCET | 年报披露先进封装、chiplet、汽车/通信布局，并持续进行产线与全球资产配置 | 客户认证、先进节点生态、EDA/测试协同及高端设备供应 | 中国AI/HPC与本地供应链机会；无一手客户/有效WPM时不绑定具体AI芯片 |

---

## 4. 设备、材料与基础设施：2026—2031需求映射

| 环节 | 主要玩家例 | 3D IC增量需求 | 产能/周期特征 | 2026—2031瓶颈信号 |
|---|---|---|---|---|
| W2W键合/对准 | EVG、SUSS、TEL等 | oxide/Cu–Cu晶圆直接键合、真空/活化、overlay | 工具交期通常短于产品认证；客户recipe保密 | particle、wafer bow、overlay和void，而非标称WPH |
| D2W/C2W键合 | Besi、ASMPT、EVG等 | KGD挑选、亚微米/微米级放置、并行/顺序键合 | 设备订单→安装→验收→量产常跨数季度 | placement精度与吞吐矛盾、die翘曲、污染、不可返工损失 |
| CMP/平坦化 | Applied、Ebara、荏原/本地厂等 | Cu recess、介质dishing、全片/局部平坦度 | recipe与pad/slurry联合认证长；耗材形成经常性收入 | 平坦度漂移会直接降低键合良率，是隐性核心瓶颈 |
| 清洗/活化 | SCREEN、TEL、Lam/SEZ、本地单片清洗厂 | 有机物、金属、纳米颗粒去除；plasma活化 | 工具+化学品+洁净物流共同决定良率 | 亚微米颗粒、queue time和再污染 |
| Cu沉积/电镀/阻挡层 | Applied、Lam、TEL及电镀/化学品厂 | TSV、RDL、bond pad、再布线 | 前道级纯度与后道成本需同时满足 | void、晶粒、退火、Cu突出/凹陷、wafer内均匀性 |
| 临时键合/解键合 | EVG、SUSS、TOK、Brewer等 | 超薄wafer carrier、背面TSV/供电、热预算 | adhesive、carrier、debond recipe认证随产品改变 | 翘曲、残胶、裂片、热循环可靠性 |
| 薄化/切割 | DISCO、Accretech等 | 多层堆叠厚度控制、DBG、laser/plasma dicing | 成熟工具但先进产品窗口更窄 | die强度、edge chipping、warpage、薄片搬运 |
| 检测/量测 | KLA、Onto、Camtek、Nova等 | pre/post bond void、overlay、表面形貌、TSV/RDL缺陷 | 检测吞吐与采样率影响有效产能 | buried interface无损检测及小缺陷可检出性 |
| 测试/探针/burn-in | Advantest、Teradyne、FormFactor、Technoprobe、Chroma等 | KGD、base die、HBM堆叠、高速链路、系统级测试 | 测试时间常随I/O、堆叠高度和温度角增长 | probe card/handler、并行度、功耗、可测性和repair覆盖 |
| ABF/载板与RDL | Ibiden、Shinko、Unimicron、Kinsus、Nan Ya、ASE/TSMC自有RDL等 | 更大package、更多层、更细线、低翘曲 | 扩厂到客户认证通常18—36个月量级 | 大尺寸良率、low-loss材料、玻璃/有机路线切换 |
| 热/供电 | TIM、lid、heat spreader、冷板、CDU、液冷连接件厂 | 3D堆叠热密度、HBM邻近热、backside power | 与芯片/package/服务器联合认证，design-in黏性强 | hotspot、热机械疲劳、泵/漏液可靠性、机架供电 |

### 4.1 设备需求的正确领先关系

```text
终端AI/汽车/手机预测
  → 客户流片与package tape-out
  → foundry/OSAT CapEx和设备订单
  → 工具交付、安装和工艺验收
  → qualification及可靠性
  → 良率/测试时间/成本达到门槛
  → 实际good package出货
```

设备订单一般领先产品出货，但领先期不稳定。直接键合的认证和稳定良率可能跨2—6个季度；新厂从土建到稳定产能常为2—4年。扩产模型若用固定6个月滞后，会系统性高估2026—2027供给。

---

## 5. 2026—2031年度供需松紧情景

下表是C组情景，不是厂商承诺。紧张度对象是“通过客户认证的good-package能力”，不是厂房名义面积。

| 年份 | 供给变化 | 需求变化 | 基准松紧判断 | 最可能迁移的瓶颈 |
|---|---|---|---|---|
| 2026 | 既有CoWoS/HBM扩产释放；Micron新加坡HBM封装开始贡献；M15X等线进入爬坡；SoIC 3nm堆叠量产扩展 | AI加速器、定制ASIC、HBM4、高端CIS继续增长 | **偏紧**：量增但新产品认证和大package消耗更多面积 | CoWoS大面积产能、HBM good stacks、先进测试、基板和液冷 |
| 2027 | 2025—26安装工具通过更多认证；OSAT增加2.5D/SiP能力；D2W多客户导入 | 云厂自研ASIC、逻辑—缓存、AI网络/CPO开始放量 | **紧平衡**：通用环节改善，高端D2W/HBM4仍紧 | KGD、D2W吞吐/良率、base die、burn-in、光电测试 |
| 2028 | Amkor Arizona等新项目接近/进入生产；亚洲新封装线爬坡；HBM前后道扩产成熟 | AI从训练扩至推理，车载/机器人3D感知增长，HBM4E更高堆叠 | **结构性分化**：成熟2.5D缓和，最高端仍紧 | 16-high薄化/堆叠、热、超大基板、直接键合可靠性 |
| 2029 | 多区域先进封装供应形成；工具二次采购转向效率与良率 | CPO、3D logic、backside互连/供电和近存计算增加 | **总体平衡、局部紧** | 标准化3D PDK、跨die签核、无损检测、系统级测试 |
| 2030 | 若2026—28 CapEx兑现，通用封装可能出现利用率压力 | AI需求增速正常化但单位package价值继续上升 | **可能出现成熟产能过剩**；高端资格产能保持溢价 | 成本/良率而非设备数量，旧线改造与折旧负担 |
| 2031 | W2W、D2W、TCB/RDL形成按应用分工；区域化产能更完整 | 3D cache/logic、CPO、HBM5/近存和感知形成多支柱 | **动态平衡**：赢家是能交付良率与测试闭环者 | 设计—制造—测试数据闭环、热/电共同优化、供应链可信性 |

### 5.1 上行、基准、下行情景的可监测触发器

| 情景 | 触发器 | 供给后果 | 商业机会 |
|---|---|---|---|
| 上行 | 多家云厂ASIC按期量产；HBM4/4E客户验证顺利；CPO进入标准交换机/加速器 | 2027—2029持续紧张，设备复购和材料耗用超预期 | D2W、CMP/清洗、KGD、高速测试、液冷和大尺寸基板 |
| 基准 | AI需求高增但周期波动；TCB与Hybrid Bonding并存；扩厂按计划爬坡 | 2026偏紧、2027紧平衡、2028后结构分化 | 能兼容多工艺、多客户的设备/材料及OSAT平台 |
| 下行 | AI CapEx消化、客户延后、HBM库存、先进封装扩产同时释放；HB良率/成本不过关 | 2028—2030名义产能过剩，价格/利用率下降 | 旧线效率提升、检测/良率软件、设备服务；高资本单一路线承压 |

---

## 6. CapEx到收入的敏感性：为什么不能简单相除

### 6.1 资本开支的四类去向

1. **建筑/公用工程：** cleanroom、超纯水、电力、气体、振动控制；不直接产生good die。
2. **瓶颈工具：** lithography、bonding、CMP、clean、plating、grind、inspection、test；单机吞吐并不代表整线吞吐。
3. **研发/qualification：** 工程wafer、失效分析、可靠性、客户样品，占用工具但不形成可售产品。
4. **营运资本与人员：** 原料、备件、工程师和轮班；新线早期OEE和yield通常低于成熟线。

因此：

```text
项目投资 ÷ 假定设备单价 ≠ 工具台数
工具台数 × 标称WPH ≠ 认证产能
认证产能 × 运行小时 ≠ good package
good package × 市价 ≠ 企业收入（产品组合、客户合同与良率不同）
```

### 6.2 建议总报告采用的“供给兑现系数”

为了情景建模而非制造事实，可定义：

```text
有效供给 = 名义能力 × 安装兑现率 × 认证通过率 × OEE × 最终良率 × 产品组合系数
```

所有系数都必须做区间敏感性，不能用一个行业平均值覆盖CIS、HBM、logic-on-cache和CPO。若缺公司数据，模型只输出指数（2026=100）和上/基/下界，不能宣称实际WPM。

---

## 7. 2026—2031最值得跟踪的商业机会

### A级：需求确定性高、跨路线通用

1. **KGD与高速测试：** 不论TCB还是Hybrid Bonding，堆叠价值越高，pre-bond筛选价值越高；HBM、logic die和base die均受益。
2. **CMP、清洗与量测耗材：** Hybrid Bonding把前道级洁净和平坦度带到先进封装，耗材复购性优于一次性设备。
3. **临时键合、超薄化和翘曲控制：** HBM高堆叠、3D logic、背面供电共同拉动。
4. **先进热管理：** 3D热密度与AI机架功率同步提升，TIM、lid、冷板、CDU、连接件和热仿真都具有系统级design-in壁垒。
5. **大尺寸低翘曲基板/RDL：** package面积和HBM数量增长直接增加面积消耗，即使AI芯片单位数增长放缓，单位面积仍可能上升。

### B级：高增长但取决于技术路线胜负

1. **亚微米D2W键合设备与并行键合架构；** 成败取决于吞吐×精度×良率的综合CoO。
2. **buried-interface无损检测；** 若直接键合扩大，其价值显著提高，但客户可能自研/集成。
3. **Hybrid Bonding专用Cu/介质材料、pad和表面处理；** 认证周期长、粘性高，市场规模受实际渗透限制。
4. **CPO/光电3D集成测试与被动对准；** 2028—2031可能形成新支柱，但量产节奏高度依赖系统架构。

### C级：需防止“概念产能”估值

1. 仅有“Hybrid Bonding能力”新闻、无客户/验收/量产收入的产线；
2. 把HBM4名称、12/16-high或TSV自动当作Cu–Cu的设备材料供应商；
3. 用CoWoS WPM推SoIC，或用OSAT总CapEx推D2W份额；
4. 大额新厂但缺电力、水、人才、基板、测试与客户认证的项目。

---

## 8. 监工应质询C组的六个问题及预答

1. **为什么不给2026—2031全球Hybrid Bonding WPM？** 公开资料没有统一W2W/D2W、wafer size、die尺寸、良率和产品口径；给单一数是伪精确。
2. **为何引用CoWoS扩产却不纳入Hybrid Bonding？** CoWoS是2.5D/系统封装供给和3D IC生态的一部分，但不是SoIC/Cu–Cu直接键合的同义词，故单列。
3. **HBM是否构成Hybrid Bonding产能？** 只有具体产品被一手制造资料确认使用direct Cu–Cu时才计入；其余只作为共同设备/材料需求。
4. **项目投产为什么仍可能缺货？** 客户需要的是good packages；新线的M3装机到M6稳定良率可能跨2—6季度，测试、基板或HBM任一不足都会限产。
5. **2030为何可能过剩？** 2024—2027全球同时扩产，而AI需求增长率可能正常化；大面积package、先进代际和认证差异又会使过剩集中在成熟能力，高端仍紧。
6. **最可投资的环节为何不是纯键合机？** 测试、清洗、CMP、检测、薄化、基板和热横跨TCB、W2W、D2W、HBM、CPO多路线，需求对单一路线胜负不敏感。

---

## 9. 来源与证据分级（至少25条）

### A1：公司财报、监管/政府文件——可证明收入、CapEx或项目金额

1. TSMC Annual Reports：<https://investor.tsmc.com/english/annual-reports>
2. TSMC Quarterly Results：<https://investor.tsmc.com/english/quarterly-results>
3. Intel Annual Reports / 10-K：<https://www.intc.com/filings-reports/annual-report>
4. Intel Fab 9 New Mexico官方发布：<https://newsroom.intel.com/corporate/intel-opens-fab-9-new-mexico>
5. Samsung Electronics IR financial information：<https://www.samsung.com/global/ir/financial-information/>
6. SK hynix IR financial information：<https://www.skhynix.com/ir/UI-FR-IR01/>
7. Micron SEC filings / annual reports：<https://investors.micron.com/financials/sec-filings>
8. Sony Group financial results：<https://www.sony.com/en/SonyInfo/IR/library/presen/er/>
9. ASE Technology financial information：<https://www.aseglobal.com/en/investors/financial-information>
10. Amkor annual reports：<https://ir.amkor.com/financial-information/annual-reports-and-proxy-statements>
11. U.S. Department of Commerce CHIPS final award to Amkor（约4.07亿美元）：<https://www.nist.gov/chips/amkor-technology>
12. JCET investor relations / reports：<https://www.jcetglobal.com/en/site/investor>
13. Besi FY2025 results（设备收入/订单）：<https://www.besi.com/investor-relations/press-releases/details/be-semiconductor-industries-nv-announces-q4-25-and-full-year-2025-results/>
14. SUSS MicroTec financial reports：<https://www.suss.com/en/investor-relations/financial-reports/>
15. ASMPT financial reports：<https://www.asmpt.com/investor-relations/financial-reports/>

### A2：公司技术/项目公告——可证明平台、产品、建设或量产声明，不自动证明有效产能

16. TSMC SoIC：<https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/SoIC.htm>
17. TSMC CoWoS：<https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/CoWoS.htm>
18. TSMC 3DFabric：<https://www.tsmc.com/english/dedicatedFoundry/technology/3DFabric>
19. Intel Foundry advanced packaging：<https://www.intel.com/content/www/us/en/foundry/advanced-packaging.html>
20. Samsung Foundry advanced packaging：<https://semiconductor.samsung.com/foundry/advanced-packaging/>
21. Samsung HBM产品页：<https://semiconductor.samsung.com/dram/hbm/>
22. SK hynix M15X投资公告：<https://news.skhynix.com/sk-hynix-to-invest-20-trillion-won-in-new-cheongju-fab-m15x/>
23. SK hynix HBM4开发/量产准备公告：<https://news.skhynix.com/en/sk-hynix-completes-worlds-first-hbm4-development-and-readies-mass-production/>
24. Micron Singapore HBM先进封装设施新闻中心：<https://newsroom.micron.com/>（在站内检索“Singapore HBM advanced packaging facility”并以公司原文为准）
25. Sony Semiconductor Solutions堆叠传感器/技术：<https://www.sony-semicon.com/en/technology/>
26. Amkor Arizona先进封装项目官方新闻：<https://ir.amkor.com/news-releases>（站内检索Arizona advanced packaging and test facility）
27. Amkor Vietnam项目：<https://amkor.com/amkor-technology-vietnam/>
28. ASE VIPack：<https://ase.aseglobal.com/vipack/>
29. JCET先进封装能力：<https://www.jcetglobal.com/en/site/technology>
30. EV Group Hybrid Bonding：<https://www.evgroup.com/technologies/hybrid-bonding/>
31. Besi Hybrid Bonding产品：<https://www.besi.com/products/hybrid-bonding/>
32. SUSS wafer bonding solutions：<https://www.suss.com/en/products-solutions/wafer-bonding/>
33. Applied Materials advanced packaging：<https://www.appliedmaterials.com/us/en/semiconductor/markets/advanced-packaging.html>
34. Lam Research advanced packaging：<https://www.lamresearch.com/solutions/advanced-packaging/>
35. DISCO IR与薄化/切割产品：<https://www.disco.co.jp/eg/ir/>
36. KLA advanced packaging process control：<https://www.kla.com/advanced-packaging>
37. Advantest IR：<https://www.advantest.com/investors/>
38. FormFactor advanced packaging/HBM test：<https://www.formfactor.com/markets/advanced-packaging/>

### A3/A4：标准与路线图——可用于技术周期，不能证明企业销量

39. JEDEC HBM focus area：<https://www.jedec.org/standards-documents/focus-areas/memory-configurations/hbm>
40. IEEE Heterogeneous Integration Roadmap：<https://eps.ieee.org/technology/heterogeneous-integration-roadmap.html>
41. SEMI Advanced Packaging：<https://www.semi.org/en/advanced-packaging>

### B1：署名新闻/第三方预测——只能旁证，不能覆盖公司事实

42. Reuters Technology（搜索TSMC CoWoS、HBM、先进封装扩产；必须保留日期和署名）：<https://www.reuters.com/technology/>
43. TrendForce News（HBM/CoWoS供需预测，必须注明为预测）：<https://www.trendforce.com/news/>
44. Yole Group新闻/市场摘要（注意付费报告口径）：<https://www.yolegroup.com/>

---

## 10. 可直接进入总报告的C组结论

> 2026—2031年3D IC供给不是“键合机数量”的单变量增长，而是先进逻辑、CoWoS/RDL、HBM good stack、W2W/D2W、基板、KGD/测试和热管理共同决定的串联系统。2026偏紧、2027紧平衡、2028后结构分化是较合理的基准情景；但每年都可能因AI CapEx、HBM客户认证或新线良率变化而前后移动。公开能够审计的是项目投资、设备收入、平台量产声明和部分产品收入；不能审计的是全球统一Hybrid Bonding有效WPM。因此，TSMC CoWoS必须与SoIC拆分，Intel Foveros必须与Foveros Direct拆分，HBM必须与Cu–Cu采用拆分，OSAT总产能也必须与客户认证的3D IC产能拆分。

> 商业机会最稳健的部分，是跨路线共用的CMP/清洗、临时键合与薄化、缺陷检测、KGD/高速测试、基板和热管理；弹性最大的部分，是亚微米D2W、Hybrid Bonding专用材料和CPO三维集成。2030—2031并非所有环节一起短缺：成熟2.5D能力可能过剩，而最先进D2W、超薄高堆叠、HBM4E/5、光电测试和液冷仍可保持稀缺。判断企业价值时，应跟踪“设备复购—客户qualification—稳定良率—实际收入”四联证据，而不是厂房面积或概念产能。
