# 全球混合键合全产业链研究（A 组）：已量产应用、产品与证据边界

**版本：** 2026-07-28  
**研究边界：** 本文只讨论 `hybrid bonding / direct bonding`（通常是介质—介质接触后 Cu–Cu 直接互连）在产品中的可核验使用，以及与之最容易混淆的“普通堆叠”“TSV 堆叠”“micro-bump/TCB”“晶圆键合”“2.5D 封装”。结论优先以公司原始公告、产品页、财报、技术白皮书或标准资料为依据。  
**浏览器限制披露：** 本轮按要求只尝试隔离内置浏览器；环境返回 `Browser is not available: iab`。未使用桌面 Chrome、个人标签页、Cookie 或个人会话。下列一手 URL 为可复核的来源台账；主报告使用前应逐页复开、保存日期/页面版本。对本轮无法逐页重开的细节，一律采用保守表述和较低结论等级。

---

## 一、结论先行：混合键合真正已经在哪些产品里发生？

1. **CIS（图像传感器）是最成熟、最容易证明已经商业化的直接键合应用。** Sony 等厂商的堆叠式 CMOS 图像传感器已经长期进入手机、相机和工业视觉供应链。Sony 的公开技术资料明确以 Cu–Cu connection/堆叠像素—逻辑结构表述相关技术。这里的商业事实是“堆叠 CIS 已商业化、部分公开技术材料披露直接 Cu–Cu 互连”；但公司通常不按 Cu–Cu 模式单独公布 wafer、sensor、客户或收入，因此不能给出全球 hybrid-bonded CIS 的精确出货量。
2. **3D NAND 是晶圆级分离制造/键合架构大规模商业化的重要场景，但不能把所有 ‘array–CMOS bonding’ 自动写成 Cu–Cu hybrid bonding。** YMTC Xtacking、Kioxia CBA、Micron CuA、SK hynix 4D NAND、Samsung COPS 都把存储阵列与 CMOS/periphery 的空间关系作为关键架构；其中 YMTC/Kioxia 的公开资料明确使用 wafer bonding 或 CBA 表述。若原始资料不逐字写 Cu–Cu/oxide hybrid bonding，就只能称“晶圆级键合/阵列—外围分离架构”，不能计入已证实 Cu–Cu 混合键合的数量。
3. **逻辑上叠存储（logic-on-memory / memory-on-logic）最清楚的商业例子是 AMD 3D V-Cache，经 TSMC SoIC 实现。** Ryzen 7 5800X3D 和 EPYC Milan-X 是公开可售产品；AMD/TSMC 明确把 3D V-Cache 与 SoIC/3D chiplet 技术联系起来。其严格可写结论是“产品已商业销售、采用 3D 堆叠 SRAM cache 的路线”；单品销售额、SoIC die 数、键合 pitch、良率和收入均未公开。
4. **Intel Foveros、Samsung X-Cube、TSMC SoIC/3Dblox 都是重要的 3D 集成平台，但须把 ‘平台存在’ 和 ‘direct hybrid bonding 已量产的特定产品’ 分开。** Intel Lakefield/Meteor Lake 的 Foveros 产品已商业出货，但公开资料并不意味着其全部采用 Foveros Direct；Foveros Direct 是更细 pitch 的路线，不能由 Foveros 产品的出货自动反推其已放量。Samsung X-Cube 已公开为 3D 封装技术平台，尚未取得可逐产品确认 Cu–Cu 直接键合量产/出货的公开一手资料。
5. **HBM 和 Cu–Cu hybrid bonding 不是同义词。** HBM 是高带宽 DRAM 堆叠、接口和系统封装产品；当前大量 AI HBM 交付可通过 TSV + micro-bump/TCB 等路线实现。HBM4 的带宽/接口变化提高直接键合的经济动机，但不能把 HBM3E/HBM4、12-high 或高 I/O 自动写成混合键合量产。公开可验证的 HBM 收入、产品送样或量产状态，仍不能转换为 hybrid-bonded stack 出货。
6. **供应链价值的核心不止键合机。** 直接键合量产的共同门槛是前道 wafer quality、CMP/清洗/表面活化、纳米级对准、薄化、键合后检测、良率/失效分析、KGD、可靠性、测试、热—供电—EDA 协同和客户 qualification。设备商的工具出货或订单是设备周期信号，不是 hybrid-bonded die 的实际出货。

---

## 二、证据标签与工艺识别规则

为避免“把新闻叙事写成实际产量”，本文使用下列标签：

|标签|本报告含义|可以说什么|不能说什么|
|---|---|---|---|
|A1|监管披露/财报中确认的收入、实物交付或产量|“公司确认收入/产品销售”|不能把收入除以假设 ASP 变 die、wafer、stack 数|
|A2|公司产品页、新闻稿、客户联合公告、正式可售/量产声明|“公司宣布可售、产品上市、公司称采用某路线”|不能延伸为满产、实际良率、全部客户采用|
|A3|政府、交易所、补贴、环评、项目文件|“项目获批、开工、建设”|不等于现有产能或实际出货|
|A4|标准、论文、专利、技术演讲、工艺白皮书|“技术文件披露某结构/pitch/方案”|不等于商业产品、客户、成本或规模出货|
|A5|署名媒体、行业新闻、第三方研究|“据媒体/机构报道”|不能脱离归因写成公司事实|
|A6|研究推演、不可独立核验线索|“技术上可能/待验证”|不得进实际出货或份额统计|

### 2.1 必须区分的四种“堆叠”

|类型|典型互连|是否自动等同 hybrid bonding|例子|
|---|---|---|---|
|晶圆级 W2W direct/hybrid bonding|介质—介质 + Cu–Cu，或其他直接键合|否；需原始资料确认 Cu/oxide 机制|部分堆叠 CIS、某些 array–CMOS 分离的 NAND 架构|
|D2W/C2W direct/hybrid bonding|裸片/已知良品 die 键合到晶圆或 carrier|否；需确认键合对象和 Cu–Cu/oxide|AMD 3D V-Cache/TSMC SoIC 路线可作为代表性商业 3D cache 例子|
|TSV + micro-bump/TCB 堆叠|焊料/铜柱/微凸点、TSV、热压键合|**否**|当前大量 HBM stack、Foveros 早期产品|
|2.5D interposer/RDL/bridge|横向裸片互连，可能带 HBM|**否**|CoWoS、EMIB、I-Cube/H-Cube 的相当部分实现|

---

## 三、全球产品与应用台账：状态、键合对象、证据及边界

### 3.1 A 类：CIS——目前最成熟的商业直接键合应用之一

|公司/技术|键合对象与方式|W2W/D2W/C2W|公开 pitch|可核验产品/商业状态|时间与一手来源|证据等级与严格边界|
|---|---|---|---|---|---|---|
|Sony Semiconductor Solutions / Exmor RS 堆叠 CIS|像素层与逻辑/电路层分离；Sony 技术资料披露 Cu–Cu connection 的堆叠传感器技术路线|以 W2W 为主的堆叠 CIS 制造逻辑；具体各型号工艺须逐一核验|未见公司对全部商用 sensor 统一公开 pitch|Exmor RS 堆叠 CMOS 图像传感器已长期产品化，用于移动与成像市场；Sony 2021 公布两层晶体管像素堆叠 CMOS 图像传感器技术|2021-12-15，Sony 新闻稿：[World’s First 2-Layer Transistor Pixel Stacked CMOS Image Sensor Technology](https://www.sony-semicon.com/en/info/2021/202112/20211215.html)；技术页：[2-Layer Transistor Pixel](https://www.sony-semicon.com/en/technology/mobile/2-layer-transistor-pixel.html)；产品入口：[Image Sensors](https://www.sony-semicon.com/en/products/is/)|A2/A4：可证明公司公开了堆叠 CIS 产品/技术路线；不提供按 Cu–Cu 工艺拆分的 sensor 出货、客户和收入。不可把 iPhone/Android 全部 Sony sensor 自动归为 direct-bonded。|
|Sony / stacked CIS 的产业意义|像素层与电路层垂直分离，direct Cu interconnect 降低跨层互连距离并提升像素/逻辑可分别优化的空间|通常归为 W2W sensor stacking|未公开统一工艺 pitch|CIS 是 direct bonding 从研发到高消费电子 volume manufacturing 的最强商业旁证之一|Sony 技术入口同上；Sony 公司技术页：[Stacked CMOS Image Sensor](https://www.sony-semicon.com/en/technology/mobile/stacked-cmos.html)|A2/A4：只确认技术和产品族，不能由技术优势推年出货。|
|OmniVision / PureCel stacked CIS|OmniVision 多代手机 CIS 有 stacked-die 产品技术；公开资料需逐型号确认是否明确写 Cu–Cu hybrid bonding|公开资料未统一给出|未公开统一 pitch|多个手机 CIS 已正式发布/供货，但本表不以“stacked”自动确认 Cu–Cu direct bonding|产品/技术入口：[OmniVision Technologies](https://www.ovt.com/)；例：2023-11-30 [OV50H press release](https://www.ovt.com/press-releases/omnivision-launches-ov50h-the-industrys-first-1-3-inch-50-megapixel-image-sensor/)|A2（产品存在）；**direct hybrid bonding 机制留空**。这行用于提醒：产品堆叠与工艺确认是两件事。|
|Samsung Electronics / ISOCELL stacked CIS|Samsung 公开大量 BSI/stacked CIS 产品；各代采用的 interconnect 不应仅凭“stacked”字样归为 Cu–Cu hybrid bonding|未统一公开|未公开统一 pitch|ISOCELL 商用产品持续出货；但本轮没有可逐型号核验的直接混合键合一手公告|产品入口：[Samsung ISOCELL](https://semiconductor.samsung.com/image-sensor/)；例：[ISOCELL HP2 announcement](https://semiconductor.samsung.com/newsroom/tech-blog/introducing-200mp-isocell-hp2-the-new-image-sensor-for-premium-smartphones/)|A2（产品/技术）；**direct hybrid bond 产品证据未取得**。|
|Canon / stacked CMOS（相机、SPAD）|Canon 已公开堆叠 CMOS/SPAD 技术和产品；键合机制应逐型号审计|未统一公开|未公开统一 pitch|产品/技术商业化与 direct bonding 不可混写|Canon 半导体/CMOS 技术入口：[Canon CMOS Sensors](https://global.canon/en/technology/cmos-sensor.html)|A2/A4：本表不能确认 Canon 某具体商用型号使用 Cu–Cu direct bonding。|

**CIS 的审计结论。** 堆叠图像传感器的商业化最早、出货最广，且 Sony 的原始技术资料构成 direct Cu connection 的强技术证据。可是即使 Sony 的 CIS 年出货很大，公开财报并不把“Cu–Cu direct-bonded CIS”列为独立收入/数量。因此 CIS 应作为“明确的成熟应用”，而不能被写成精确的 global hybrid-bonding unit market size。

### 3.2 B 类：3D NAND——实际产品广泛，但必须审计“bonding”是否就是 hybrid bonding

|公司/架构|array 与 CMOS/periphery 的关系|W2W/D2W/C2W|公开 pitch|产品/量产状态|时间与一手来源|混合键合判定与边界|
|---|---|---|---|---|---|---|
|YMTC / Xtacking®|公开技术叙事为 memory array wafer 与 peripheral CMOS wafer 分别制造，再通过 wafer bonding 集成|W2W 架构最相容；具体每代键合界面应看公司工艺资料|未见本轮可审计的统一 pitch|Xtacking NAND 已有多代商用产品/客户 SSD 生态；公司产品/技术页面证明路线及商业产品存在|技术入口：[YMTC Xtacking®](https://www.ymtc.com/en/technology/xtacking)；公司产品入口：[YMTC Products](https://www.ymtc.com/en/product)|A2：可写“array–periphery 分离制造和 wafer bonding 架构已商业化”；除非原文明确 Cu–Cu/oxide hybrid bonding，**不得直接把全部 Xtacking 出货归为 Cu–Cu hybrid bonding**。|
|Kioxia / CBA（CMOS directly Bonded to Array）|CBA 名称本身表明 CMOS 与 array 的直接键合架构；其用于 BiCS FLASH 产品代际|W2W 的架构表述|未公开统一 pitch|Kioxia 宣布以 CBA 架构推进 BiCS FLASH 产品，属于商业 NAND 路线|2020-10-20：[Kioxia Announces 6th Generation BiCS FLASH 3D Flash Memory](https://www.kioxia.com/en-jp/business/news/2020/20201020-1.html)；公司技术入口：[BiCS FLASH](https://www.kioxia.com/en-jp/business/technology/bics-flash.html)|A2：可以认定 CBA/直接键合 array–CMOS 为产品路线；**原始公告若未说明氧化物/Cu 混合键合的层间互连细节，则不将其计入已证实 Cu–Cu direct-bonded die。**|
|Micron / CMOS under Array（CuA）|CMOS circuitry 位于 memory array 下方，以提高阵列面积效率；“CuA”首先是布局架构名，不是 Cu–Cu hybrid bonding 的自动缩写|通常是单晶圆的阵列—外围布局，不应因名称假定 W2W|不适用/未公开|Micron 多代 3D NAND 已商业出货；产品路线商业性明确|技术页：[Micron 3D NAND](https://www.micron.com/products/nand-flash/3d-nand)；公司新闻入口：[Micron Newsroom](https://www.micron.com/about/newsroom)|A2：商业 NAND 可确认；**CuA ≠ Cu–Cu bonding**，不能计为 direct bonding 未经证实的出货。|
|SK hynix / 4D NAND|4D NAND 将 peripheral-under-cell 等结构作为密度/效率路线|公开资料不足以将其全部定性为 W2W Cu–Cu hybrid bonding|未公开统一 pitch|4D NAND 为已量产产品线/路线|产品/技术入口：[SK hynix NAND](https://news.skhynix.com/en/category/product/flash-memory/)；公司产品入口：[SK hynix NAND Flash](https://product.skhynix.com/products/ssd/)|A2：可写商用 3D/4D NAND 产品；direct hybrid bonding 机制在本轮留空。|
|Samsung / COPS（Cell Over Periphery）|cell array 位于 peripheral circuitry 上方的 3D NAND 架构|主要是单晶圆架构/工艺叙事，不应自然当作 W2W|未公开统一 pitch|Samsung 128-layer 等 NAND 产品商业化|Samsung 技术页：[V-NAND / COPS](https://semiconductor.samsung.com/newsroom/tech-blog/the-technology-behind-samsungs-8th-generation-v-nand/)，产品入口：[Samsung NAND Flash](https://semiconductor.samsung.com/flash-storage/)|A2：可确认商用 V-NAND 和 COPS 路线；**不是 Cu–Cu hybrid bonding 的自动证据。**|

**3D NAND 的审计结论。** 3D NAND 已把垂直结构和某些 wafer-level bonding 架构推进到极大规模；但它和“逻辑—逻辑 Cu–Cu hybrid bonding”在互连、存储单元、缺陷、测试和商业单位上不同。报告应写：**“3D NAND 是商业化的垂直/键合架构应用，YMTC Xtacking 与 Kioxia CBA 是 array–CMOS wafer bonding 的关键例子；具体是否使用 Cu–Cu/oxide hybrid bonding、pitch 和每代产品的实际出货需要逐代工艺文件确认。”**

### 3.3 C 类：logic-on-logic、logic-on-cache、CPU/GPU/AI——最关键的商业转折是 AMD 3D V-Cache

|公司/技术|键合对象与方式|W2W/D2W/C2W|公开 pitch|可核验产品/客户|时间与一手来源|量产/实际出货证据与限制|
|---|---|---|---|---|---|---|
|TSMC / SoIC®|TSMC 3DFabric 中的 system-on-integrated-chips 路线，服务逻辑—逻辑、逻辑—SRAM/缓存等 3D 集成；可提供 W2W/D2W 选项，具体取决于产品流程|平台支持 W2W/D2W；**不能只凭平台判某一客户的实际模式**|TSMC 对不同世代/设计提供不同密度；本轮不把营销指标写成 A4E/某客户 pitch|SoIC 是 TSMC 正式产品平台，AMD 3D V-Cache 是最清晰的商业生态例子|平台入口：[TSMC 3DFabric](https://3dfabric.tsmc.com/english)；SoIC 页：[TSMC SoIC](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/SoIC.htm)|A2：平台正式存在；不公开 SoIC package/die 真实出货或收入，不能用 TSMC 总营收或 CoWoS 产能推回。|
|AMD / 3D V-Cache™ + TSMC SoIC|SRAM cache die 垂直堆叠在 CPU CCD/逻辑 die 上；AMD 明确称此为 3D chiplet/3D V-Cache 路线，TSMC SoIC 是其关键制造技术|公开产业技术资料普遍将其归为 D2W/SoIC 路线；单 SKU 流程仍需产品级 PDK/制造资料确认|AMD 对 3D V-Cache 给出架构优势，但不以量产产品方式公开绑定 pitch；本表不填数|Ryzen 7 5800X3D、EPYC 7003 with AMD 3D V-Cache（Milan-X）已正式上市销售；后续 X3D 产品持续扩展|2021-06-01：[AMD Unveils 3D Chiplet Technology](https://www.amd.com/en/corporate/events/3d-chiplet.html)；2022-03-15：[AMD Ryzen 7 5800X3D launch](https://www.amd.com/en/newsroom/press-releases/2022-3-15-amd-unveils-world-s-fastest-gaming-desktop-proce.html)；2022-03-21：[AMD EPYC 7003 with 3D V-Cache](https://www.amd.com/en/newsroom/press-releases/2022-3-21-amd-epyc-processors-with-amd-3d-v-cache-technol.html)|A2（正式可售产品）+ A4（3D chiplet/SoIC 技术披露）。这是**实际产品量产/出货最强的 logic-on-cache 商业证据**之一；AMD 不披露单 SKU 出货或 3D V-Cache 收入，不能制造数量。|
|AMD / 后续 Ryzen X3D、EPYC Genoa-X 等|延续 logic-on-SRAM 3D V-Cache 产品路线|具体制造模式不应在没有公开工艺页时统一外推|未逐 SKU公开|多个 X3D SKU 正式上市，证明商业路线并非单次试产|产品入口：[AMD Ryzen Processors](https://www.amd.com/en/products/processors/desktops/ryzen.html)；EPYC 入口：[AMD EPYC](https://www.amd.com/en/products/processors/server/epyc.html)|A2：可证明产品销售；不能从 SKU 表、游戏性能或 CPU 收入反推 SoIC die 出货。|
|Intel / Foveros（非 Foveros Direct）|Intel 的 3D die stacking 平台，已用于 Lakefield、Meteor Lake 等产品；已商用产品的公开资料多为 micro-bump/传统 Foveros 叙事|具体产品常见 D2W/封装堆叠，但需以 Intel 产品/工艺原文核实|不同版本不同；不能统一填 direct-bond pitch|Lakefield、Meteor Lake 等 Foveros 产品实际上市|Foveros 技术入口：[Intel Foveros](https://www.intel.com/content/www/us/en/architecture-and-technology/foveros.html)；Lakefield 产品公告：[Intel Hybrid Technology / Lakefield](https://www.intel.com/content/www/us/en/newsroom/news/intel-hybrid-technology.html)；Meteor Lake 技术入口：[Intel Core Ultra](https://www.intel.com/content/www/us/en/products/docs/processors/core-ultra/1st-gen-core-ultra-processor-brief.html)|A2：可证明 Foveros 产品已商业化；**不得把这自动写为 Foveros Direct/Cu–Cu hybrid bonding 量产。**|
|Intel / Foveros Direct|Intel Foundry 的高密度 direct-bonding 路线，面向更小 pitch 逻辑 3D 集成|路线可适配先进 D2W/直接键合；特定量产流尚需客户/产品确认|Intel 对路线有技术规格/目标表述，需保留原文语境|本轮未取得能证明“某一公开可售产品已量产 Foveros Direct”的一手产品—工艺闭环|Foundry advanced packaging 入口：[Intel Foundry Advanced Packaging](https://www.intel.com/content/www/us/en/foundry/advanced-packaging.html)|A2/A4（平台/路线）。**量产出货留空。** 不可用 Foveros 产品销售量替代 Foveros Direct 出货。|
|Samsung / X-Cube™|Samsung Foundry 的 3D IC/TSV 互连与 chip stacking 平台；官方以 X-Cube 作为先进封装产品族之一|未在本轮找到逐产品 W2W/D2W/C2W 的一手确认|未公开统一 pitch|平台已公开；但未得到可审计的客户 SKU + direct Cu–Cu hybrid bonding mass production 公告|Samsung packaging 入口：[Samsung Foundry Advanced Packaging](https://semiconductor.samsung.com/foundry/advanced-packaging/)；技术文：[X-Cube: The Future of Semiconductor Packaging Technology](https://semiconductor.samsung.com/newsroom/tech-blog/x-cube-the-future-of-semiconductor-packaging-technology/)|A2（平台）。**不能以 X-Cube 名称或 Samsung DS 收入证明 Cu–Cu direct bonding 客户/出货。**|
|Samsung / I-Cube、H-Cube|异构 2.5D/高密度封装平台，可用于逻辑—HBM/多 die 系统|以系统封装架构为主；不代表 W2W direct bonding|不适用/未公开统一 pitch|公司公开平台能力|同一官方入口：[Samsung Advanced Packaging](https://semiconductor.samsung.com/foundry/advanced-packaging/)|A2：平台存在；**CoWoS/2.5D 类和 hybrid bonding 必须分开统计。**|
|TSMC/客户 AI 逻辑及 2.5D CoWoS|先进 AI package 中，logic + HBM + interposer/RDL 是主要商业交付；有些未来路线可能结合 SoIC，但 CoWoS 本身非 Cu–Cu direct-bonding 同义词|2.5D package，非 W2W direct-bond 判断对象|不适用|NVIDIA/AMD/HPC 生态使用 TSMC 先进封装；具体哪些 SKU 采用 SoIC 需单独确认|TSMC 3DFabric/CoWoS 入口：[TSMC CoWoS](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/CoWoS.htm)|A2：可确认 CoWoS 产品平台；不可把所有 AI GPU/HBM package 写为 hybrid-bonded。|

### 3.4 D 类：memory-on-logic、HBM 与 AI 先进封装——交集存在，不能互相替代

|场景|实际商业事实|键合机制的可证实程度|正确结论|禁止结论|
|---|---|---|---|---|
|AMD 3D V-Cache（SRAM-on-logic）|正式 CPU/server SKU 可售，是 direct 3D cache 商业化代表|公司/TSMC 技术叙事支持 SoIC/3D chiplet；产品销量未拆分|“memory-on-logic/logic-on-cache 的商业 3D 集成案例”|“所有 AMD CPU/GPU 均使用同一 hybrid-bonded cache 方案”；或从收入计算 cache die 数|
|HBM3/HBM3E 系统|HBM 已在 AI/HPC 有实际收入和出货；GPU/ASIC 经 CoWoS/2.5D 等集成|HBM stack 内部的键合需逐 DRAM 厂、逐代际确认；公开量产主流并不能全部确认是 Cu–Cu hybrid bond|“HBM 与先进封装共同推动 KGD、测试、热、基板和互连需求”|“HBM3E/HBM4 就等于 Cu–Cu hybrid bonding”|
|HBM4 与 logic base die|HBM4 提高 I/O、base-die、封装和验证协同难度；供应商产品节奏持续推进|具体 stack 内键合及 logic-to-memory 接口方案需逐产品证实|“可能提高 direct bonding 的经济动机并与 TCB/micro-bump 并行”|“HBM4 已经/必然全面切换 Cu–Cu hybrid bonding”|
|GPU/AI accelerator 的 3D integration|部分 AI 系统把 2.5D HBM、3D cache、logic stacking 和 chiplet 组合使用|必须使用 SKU/BOM/厂商工艺资料确认|“AI 是先进封装和高密度互连需求最大拉力”|“AI GPU 销售收入 = hybrid-bonded die 出货”|

参考 HBM 的标准层定义：[JEDEC HBM Focus Area](https://www.jedec.org/standards-documents/focus-areas/memory-configurations/hbm)（A4）。参考异构集成工艺挑战：[IEEE Heterogeneous Integration Roadmap](https://eps.ieee.org/technology/heterogeneous-integration-roadmap.html)（A4）。二者都不能证明某公司的实际产品或出货。

---

## 四、全球产业链：从材料与设备到产品认证

### 4.1 产业链地图与“必须同时成立”的量产条件

```text
设计/架构与 3D EDA
        ↓
逻辑/存储晶圆与 KGD
        ↓
CMP ─ 清洗/表面活化 ─ 对准/键合 ─ 薄化/背面工艺
        ↓
缺陷检测/量测 ─ 切割/封装 ─ 测试/burn-in ─ 热/PDN
        ↓
客户 qualification ─ 系统软件/可靠性 ─ 实际交付/收入
```

只有最后一段的客户验收、可售产品、交付或收入才是商业化/实际出货证据。上游设备装机、园区开工、工艺论文、专利或样片均不能替代。

|环节|全球关键参与者（非穷尽）|可公开确认的能力|商业判断边界|
|---|---|---|---|
|直接键合技术/IP|Xperi / DBI®，Sony 等 CIS 垂直整合者，TSMC/Intel/Samsung|Xperi 公开 DBI direct-bond interconnect IP/技术；foundry 公开 SoIC/Foveros Direct/X-Cube 路线|IP/技术存在不代表某客户产品采用或给出出货量。|
|键合与临时键合设备|EV Group、Besi、SUSS MicroTec、ASMPT 等|设备商公开 W2W、D2W、hybrid bonding 平台、设备订单/收入|设备销售不等于 customer production yield，更不等于 hybrid-bonded die 数。|
|前处理/CMP/清洗/沉积|Applied Materials、Lam、TEL、SCREEN、Ebara、荏原/材料公司以及本土设备材料厂|关键是表面粗糙度、颗粒、Cu/oxide 平坦化、活化和缺陷控制|一台设备的 `capability` 或产品目录不等于客户 qualification。|
|计量、检测、失效分析|KLA、Onto Innovation、Camtek、Hitachi High-Tech、各类量测厂|对准、overlay、键合空洞/缺陷、晶圆翘曲/厚度控制|若无产品/客户披露，不能把设备收入拆成 direct-bonding revenue。|
|晶圆、先进封装、OSAT|TSMC、Sony、Intel、Samsung、ASE、Amkor、JCET、PTI 等|不同厂商分别覆盖 W2W、D2W、RDL/interposer、测试与系统封装|OSAT/Foundry 总收入、厂房、CapEx 都不能回推 hybrid-bond package。|
|存储/逻辑及客户|Sony/OmniVision/Samsung（CIS），AMD、Intel、CSP/AI chip 设计商，YMTC/Kioxia/Micron/SK hynix/Samsung（存储）|产品技术路线与商业状态各自不同|同一公司不同产品可采用完全不同互连；必须逐 SKU 取证。|

### 4.2 一手来源台账：设备/IP/平台（用于技术链定位，不用于出货推算）

|参与者|一手 URL|来源性质|本报告可使用范围|
|---|---|---|---|
|Xperi DBI|[Xperi DBI Direct Bond Interconnect](https://www.xperi.com/technology/dbi/)|A2/A4 技术/IP页|可说明 DBI 为直接键合 IP/技术路线；不能推客户生产量。|
|EV Group|[EVG Hybrid Bonding](https://www.evgroup.com/technologies/hybrid-bonding/)|A2 技术页|可说明 W2W/D2W 工具/工艺平台存在；不可推设备客户、量产产品或收入。|
|Besi|[Besi Hybrid Bonding](https://www.besi.com/products/hybrid-bonding/)|A2 技术页|可说明设备产品线；应把设备订单与 die 出货隔离。|
|SUSS MicroTec|[SUSS Advanced Packaging](https://www.suss.com/en/products-solutions/advanced-packaging)|A2 产品页|可说明临时键合/光刻/先进封装工具生态；不能确认某客户 direct bonding。|
|ASMPT|[ASMPT Advanced Packaging](https://www.asmpt.com/en/products/advanced-packaging/)|A2 产品页|可确认封装设备参与；不等于 hybrid bond 产量。|
|KLA|[KLA Advanced Packaging](https://www.kla.com/advanced-packaging)|A2 产品页|可确认检测/计量在先进封装中存在；不拆分客户/工艺收入。|
|Synopsys|[Synopsys 3DIC Compiler](https://www.synopsys.com/implementation-and-signoff/3dic-compiler.html)|A2 产品页|可确认 3D IC 设计工具存在；软件许可不是产品流片/出货。|
|Cadence|[Cadence Integrity 3D-IC Platform](https://www.cadence.com/en_US/home/tools/system-analysis/3d-ic.html)|A2 产品页|可确认 3D IC EDA 能力；不能推 customer tape-out。|

这八项设备/IP/EDA 一手入口，加上前述 Sony、YMTC、Kioxia、Micron、SK hynix、Samsung、TSMC、AMD、Intel、JEDEC、IEEE 的一手/标准链接，构成超过 **15 个**原始 URL 的基础来源台账。它们的证据强度不同，不能被合并成单一“混合键合产能”数字。

---

## 五、关键公司逐项状态判断：哪些可以叫“已量产/已出货”？

|公司/平台|可以确认的产品商业状态|可以确认的 direct/hybrid bonding 状态|正确标签|最常见错误|
|---|---|---|---|---|
|Sony stacked CIS|堆叠 CIS 长期商业化，产品进入成像市场|Sony 技术材料支持 Cu–Cu connection/堆叠技术；逐 sensor/客户数量未披露|CIS 产品 A2；工艺 A4/A2；数量空缺|把 Sony 所有 CIS 或全部手机 sensor 都算作 Cu–Cu direct-bonded 出货。|
|YMTC Xtacking|多代商业 NAND 路线|公开 array/periphery separate processing + wafer bonding；每代 Cu–Cu 细节需原文|产品/架构 A2；Cu–Cu 逐代待核|把 Xtacking 品牌直接等同所有 hybrid-bonded NAND die。|
|Kioxia CBA|BiCS Flash 商业路线|CBA 为 CMOS-directly-bonded-to-array 架构；细节需逐代技术资料|产品/架构 A2；Cu–Cu 逐代待核|把 `directly bonded` 简化为所有层都有 Cu–Cu hybrid bonds。|
|AMD 3D V-Cache|Ryzen 5800X3D、EPYC Milan-X 等产品正式上市；后续 X3D 产品延续路线|SoIC/3D chiplet 技术与产品明确关联，是 logic-on-cache direct 3D 集成最强商业例证|产品 A2；技术 A4；出货/收入空缺|从 AMD CPU 收入推 3D cache die 数或把所有 AMD chiplet 都认作 V-Cache。|
|TSMC SoIC|正式 foundry/3DFabric 产品平台|支持 W2W/D2W direct 3D integration，具体客户/模式不公开|平台 A2；客户出货空缺|将 CoWoS capacity、TSMC revenue 或 SoIC roadmap 转为 hybrid-bond product units。|
|Intel Foveros|Lakefield/Meteor Lake 等 Foveros 产品已商业上市|Foveros Direct 与一般 Foveros 有技术代际区别；产品是否 Foveros Direct 要逐 SKU证实|Foveros 产品 A2；Direct 量产空缺|“Foveros 已出货” = “Foveros Direct 已大规模 Cu–Cu 出货”。|
|Samsung X-Cube/I-Cube/H-Cube|先进封装平台公开存在|未取得特定客户 SKU 已用 Cu–Cu direct bonding 的一手闭环|平台 A2；产品量产/直键合出货空缺|把平台页、foundry 营收、HBM 概念图写成直键合量产。|
|HBM 三厂及 AI GPU|HBM、AI accelerator 已有实际商业收入/交付|没有一般性公开依据证明所有 HBM/AI package 使用 Cu–Cu direct bonding|HBM 产品/收入 A1/A2（逐公司）；hybrid bond 逐产品空缺|把 HBM4、12-high、CoWoS、AI GPU 与 hybrid bonding画等号。|

---

## 六、工艺路线的时间、周期、瓶颈与竞争要素

### 6.1 当前真实的商业化梯度

```text
成熟且广泛商业化
  堆叠 CIS（其中部分公开技术为 Cu–Cu direct connection）
  3D NAND array–periphery 分离/键合架构
  AMD 3D V-Cache / TSMC SoIC 的逻辑—缓存产品
        ↓
已商业化的 3D 封装、但不可自动判为直接混合键合
  Intel Foveros（一般版本）
  HBM TSV + micro-bump/TCB 堆叠
  CoWoS / EMIB / I-Cube / H-Cube 等 2.5D 系统集成
        ↓
技术平台、客户导入和路线图，须等待逐产品量产闭环
  Intel Foveros Direct、部分 Samsung X-Cube 具体客户
  HBM4 相关 direct-bonding 变体
  AI logic-to-logic / logic-to-memory 高密度 direct bonding
```

### 6.2 量产瓶颈并不等于“买到键合机”

|瓶颈|为何决定商业化|CIS/3D NAND 的经验|logic/cache/AI/HBM 的额外难点|
|---|---|---|---|
|表面平坦度、颗粒与清洗|Cu/oxide 直接键合对界面缺陷极敏感，键合后难返修|CIS/存储在高度标准化的 wafer 流程中长期积累|逻辑 die 更昂贵，单个缺陷的报废价值高。|
|overlay/对准与热预算|影响互连良率、信号和后续 BEOL/薄化|W2W 适合相同尺寸/已成熟流程|D2W/C2W 需兼顾 KGD、chip size、翘曲与对准。|
|KGD 和测试|先堆后测可能导致高价值堆叠整体损失|存储/传感器产品测试流程较成熟|逻辑—SRAM/逻辑—逻辑/HBM 需要更复杂的 pre-bond/post-bond 和系统测试。|
|薄化、背面供电、热|越靠近高功耗逻辑，热/机械应力越难管理|CIS/存储功耗相对可控|AI logic 与多层缓存/存储的 PDN、热、散热和可靠性更严苛。|
|设计生态|需要可签核的跨 die 时序、SI、PI、热、应力、测试模型|CIS/3D NAND 产品结构更垂直整合|多厂 chiplet、HBM、OSAT、foundry 让责任/PDK/测试边界复杂。|
|客户 qualification|可靠性和供货连续性决定从样品到稳定量产的斜率|移动 CIS / NAND 有成熟客户认证体系|数据中心客户对性能、固件、供应安全和长期可靠性门槛更高。|

### 6.3 扩产/爬坡应怎么写

“厂房宣布、设备到厂、键合机订单、政府补贴、样品、客户认证、准备量产”都不是实际出货。正确状态顺序是：

1. 公告/设计能力；
2. 厂房与设备安装；
3. 工艺调试、材料导入与可靠性；
4. 客户 qualification 的可用产能；
5. 考虑良率、测试和产品组合后的有效产能；
6. 期间实际 wafer/die/package 出货或收入确认。

公开资料极少披露第 5、6 项。因此，对所有 company 的 `WPM`、设备数、投资额或面积，若没有技术节点、良率、产品和时间边界，只能放在 A3/A5 项目台账，不能用于计算 hybrid-bonded die 产量。

---

## 七、最值得用于后续追踪的“升级证据”

|待解决问题|可以把结论升级的最优证据|不能替代它的材料|
|---|---|---|
|某 CIS 是否为 Cu–Cu direct-bonded|该 sensor 的原始 datasheet/技术论文、公司工艺页，最好有封装/键合截面|手机拆解、营销词“stacked”、供应链传言|
|某 3D NAND 是何种键合|厂商工艺论文/专利/技术演讲，明确 W2W、oxide/Cu、互连位置|“Xtacking/CBA/CuA/4D”品牌名本身|
|Foveros Direct 是否已商业量产|Intel 产品公告/客户联合公告明确 Direct 版本，或财报/技术论文的产品映射|一般 Foveros SKU、工厂开工、Foundry 总收入|
|X-Cube 是否 direct-bond 客户出货|Samsung + 客户产品/工艺联合公告|平台介绍、测试芯片、新闻中的未来路线|
|HBM 是否用 hybrid bonding|DRAM 厂的产品工艺/可靠性披露 + 客户 package/封装资料|HBM4 名称、12-high、高 I/O、送样消息|
|某设备/材料商实现商业价值|供应商 A1 收入中可拆分的产品线，或客户一手验收/复购/量产设计赢|设备目录、专利、技术演示、模糊的“获订单”|

---

## 八、可直接纳入总报告的最终表述

> 全球混合键合的已商业化足迹并非从 AI/HBM 才开始：堆叠 CIS 是成熟的直接 Cu 互连商业应用，3D NAND 已广泛采用垂直及 array–periphery 分离/键合架构，AMD 3D V-Cache 与 TSMC SoIC 则是 logic-on-cache 3D 集成进入标准 CPU/server 产品的清晰例证。与此同时，很多被归入“3D 封装”的产品仍使用 TSV、micro-bump、TCB、interposer 或 RDL；Intel Foveros、Samsung X-Cube 和 AI/HBM package 的实际出货不能自动等同于 Foveros Direct 或 Cu–Cu hybrid bonding 出货。

> 因此，竞争核心不是单一键合设备，而是材料与表面质量、对准、薄化、缺陷检测、KGD/测试、热与供电、3D EDA 和客户 qualification 的系统良率。公开数据能够确认多个平台和产品已经商业化，但通常不能披露 direct-bonded die、package 或 stack 的实际数量。任何用公司收入、设备订单、厂房投资、CoWoS 名义产能、HBM 收入或产品新闻反推 hybrid-bonding 实物出货的做法，都应被排除。

---

## 附录：本组一手 URL 清单（25 项）

1. [Sony 2-Layer Transistor Pixel Stacked CMOS announcement](https://www.sony-semicon.com/en/info/2021/202112/20211215.html)  
2. [Sony 2-Layer Transistor Pixel technology](https://www.sony-semicon.com/en/technology/mobile/2-layer-transistor-pixel.html)  
3. [Sony Stacked CMOS technology](https://www.sony-semicon.com/en/technology/mobile/stacked-cmos.html)  
4. [Sony Image Sensors product portal](https://www.sony-semicon.com/en/products/is/)  
5. [OmniVision OV50H product announcement](https://www.ovt.com/press-releases/omnivision-launches-ov50h-the-industrys-first-1-3-inch-50-megapixel-image-sensor/)  
6. [Samsung ISOCELL portal](https://semiconductor.samsung.com/image-sensor/)  
7. [Canon CMOS sensor technology](https://global.canon/en/technology/cmos-sensor.html)  
8. [YMTC Xtacking](https://www.ymtc.com/en/technology/xtacking)  
9. [YMTC Products](https://www.ymtc.com/en/product)  
10. [Kioxia sixth-generation BiCS FLASH announcement](https://www.kioxia.com/en-jp/business/news/2020/20201020-1.html)  
11. [Kioxia BiCS FLASH technology](https://www.kioxia.com/en-jp/business/technology/bics-flash.html)  
12. [Micron 3D NAND](https://www.micron.com/products/nand-flash/3d-nand)  
13. [SK hynix Flash Memory news/product channel](https://news.skhynix.com/en/category/product/flash-memory/)  
14. [Samsung V-NAND technology](https://semiconductor.samsung.com/newsroom/tech-blog/the-technology-behind-samsungs-8th-generation-v-nand/)  
15. [TSMC 3DFabric](https://3dfabric.tsmc.com/english)  
16. [TSMC SoIC](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/SoIC.htm)  
17. [TSMC CoWoS](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/CoWoS.htm)  
18. [AMD 3D Chiplet Technology](https://www.amd.com/en/corporate/events/3d-chiplet.html)  
19. [AMD Ryzen 7 5800X3D launch](https://www.amd.com/en/newsroom/press-releases/2022-3-15-amd-unveils-world-s-fastest-gaming-desktop-proce.html)  
20. [AMD EPYC with 3D V-Cache launch](https://www.amd.com/en/newsroom/press-releases/2022-3-21-amd-epyc-processors-with-amd-3d-v-cache-technol.html)  
21. [Intel Foveros](https://www.intel.com/content/www/us/en/architecture-and-technology/foveros.html)  
22. [Intel Foundry Advanced Packaging](https://www.intel.com/content/www/us/en/foundry/advanced-packaging.html)  
23. [Samsung Foundry Advanced Packaging](https://semiconductor.samsung.com/foundry/advanced-packaging/)  
24. [Xperi DBI Direct Bond Interconnect](https://www.xperi.com/technology/dbi/)  
25. [EV Group Hybrid Bonding](https://www.evgroup.com/technologies/hybrid-bonding/)  
26. [Besi Hybrid Bonding](https://www.besi.com/products/hybrid-bonding/)  
27. [JEDEC HBM focus area](https://www.jedec.org/standards-documents/focus-areas/memory-configurations/hbm)  
28. [IEEE Heterogeneous Integration Roadmap](https://eps.ieee.org/technology/heterogeneous-integration-roadmap.html)

**审计警告：** 每个 URL 的存在只支持本表指定的证据层级，不能自动支持其他列的量产、客户、出货、pitch、收入或供应关系。发布前需逐链接复核页面可用性、发布日期和原文措辞。
