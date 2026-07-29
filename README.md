# 混合键合（Hybrid Bonding）全产业链研究

本仓库是一组截至 **2026-07-29** 的3D IC与混合键合产业链审计研究，重点回答：

- 哪些 Hybrid Bonding 产品已经实际商业化，哪些仍是平台、送样、验证或研发；
- W2W、D2W/C2W、TSV、micro-bump/TCB、2.5D 封装和 HBM 之间的技术边界；
- 全球和中国大陆从 IP、EDA、晶圆、设备、材料、检测、测试、封测到系统客户的完整参与者；
- 产能、扩产、工艺认证和良率爬坡的真实含义；
- CIS、3D NAND、logic/cache、HBM、photonics、MEMS 在 2025–2031 年的渗透节奏与转折点；
- 算苗科技提出的 8 层存储晶圆、160GB、16TB/s、Cu–Cu 混合键合路线处在产业链哪个位置。
- 中科声龙与算苗科技的专利组合、权属变化及其与3D存算/Hybrid Bonding路线的真实关联。
- 2026基准年至2031五年终点的逐年销售额、有效能力指数、应用增长、供需松紧和商业机会。

## 核心结论

1. **CIS 是当前最成熟的商业直接键合应用。** Sony 的堆叠式 CIS 是公开证据最强的案例之一。
2. **部分 3D NAND 已将 array 与 CMOS/periphery 分开制造并进行晶圆级键合，**但不能把所有 3D NAND 或所有 Xtacking/CBA/CuA/4D/COPS 名称自动归为同一种 Cu–Cu Hybrid Bonding 工艺。
3. **AMD 3D V-Cache + TSMC SoIC 是 logic-on-cache 最清楚的公开商用案例之一。**
4. **HBM 与 Hybrid Bonding 不是同义词。** 当前大量 HBM 仍以 TSV + TCB/micro-bump 量产；HBM4、12-high 或 16-high 都不能自动计入 Hybrid Bonding 实际出货。
5. **真正的壁垒是整条工艺闭环，**包括 CMP、Cu recess、清洗、颗粒、overlay、W2W/D2W、薄化、检测、KGD、测试、热、可靠性和客户资格。
6. **全球没有统一可审计的 Hybrid Bonding wafer/die/package 实际出货和有效产能口径。**本研究拒绝用设备订单、公司营收、全厂 WPM 或 CapEx 反推 bonded die。
7. **中科声龙与算苗存在技术脉络，但专利权属不能混写。**中科声龙 `CN219040074U` 已明确披露存储—计算芯片Hybrid Bonding，后转让给新加坡声龙；算苗 `CN121920305A`、`CN121925162A`则直接披露计算—存储混合键合和3D缓冲层设计。专利披露仍不等于A4E量产或Cu–Cu实物验证。

## 仓库结构

```text
report/
  3D_IC_2026-2031增长产能销售额与商业机会_30条Debate审计版.md
  Hybrid_Bonding全产业链深度研究_2025-2031_30轮审计版.md
  算苗科技_8层160GB_16TBs_CuCu混合键合与中国存储链_重做审计版.md
  中科声龙与算苗科技_3D存算及混合键合专利审计.md
debate/
  debate_30_rounds.md
  final_verdict.md
  3dic_2026_2031_verification_initial.md
  3dic_2026_2031_debate_30_rounds.md
  3dic_2026_2031_final_verdict.md
evidence/
  global_products.md
  equipment_materials.md
  china_supply_chain.md
  market_capacity.md
  competition_roadmap.md
  3dic_2026_2031_market_model.md
  3dic_2026_2031_applications.md
  3dic_2026_2031_capacity.md
  3dic_2026_2031_competition.md
  3dic_2026_2031_china_opportunities.md
sources/
  source_index.md
```

## 数据方法

研究采用分级审计：

- A1：经审计财报、监管披露、实际收入或实物交付；
- A2：公司官网、产品发布、正式量产或客户联合公告；
- A3：政府备案、项目建设、环评、补贴；
- A4：论文、专利、标准、技术资料；
- A5：署名新闻和第三方研究；
- A6：研究情景、计算或待验证线索。

关键原则：

```text
流片 ≠ 晶圆完成 ≠ 封装完成 ≠ 点亮 ≠ 客户认证 ≠ 量产 ≠ 出货

设备订单 ≠ 已装机 ≠ 已验收 ≠ 有效产能 ≠ bonded die 实际产出

HBM ≠ Hybrid Bonding
```

## 30 轮 Debate

本研究由五个研究组分别覆盖全球产品、设备材料、中国链、商业产能和竞争路线图。每组接受六轮交叉质询，共 30 条监工记录。Debate 的作用是发现口径混淆、来源降级和不当推导，不能替代原始证据。

2026–2031专项另由五组覆盖市场模型、应用、产能、全球竞争和中国机会，并由第六个独立监工按六主题×五组完成30条连续审计。专项模型把M1狭义制造/封装服务、M2设备材料增量、M3终端半导体价值池分开，全部绝对额标记为A6情景，不能相加或冒充实际统计。

## 免责声明

本仓库用于产业研究与信息审计，不构成证券、投资或商业采购建议。未披露不等于不存在；报告中的“公开未确认”表示在资料截点之前没有取得足以进入事实表的一手证据。
