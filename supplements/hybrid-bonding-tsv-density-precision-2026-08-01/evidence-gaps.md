# 公开证据缺口与下一步取证

“未确认”仅表示本资料截点前未获得足以进入事实表的公开闭环，不代表技术、商业活动或客户关系物理上不存在。

| ID | 尚不能公开确认的问题 | 需要怎样的证据才能升级结论 | 当前报告的处理 |
|---|---|---|---|
| U01 | 某 Hybrid Bonding 产品是否已经出货、出货多少 die/wafer、收入多少 | 制造商与客户联合公告，或法定/审计文件，带 SKU、期间、交付/收入口径 | 不用设备订单、新闻或专利代替 |
| U02 | TSMC SoIC 量产产品的实际 pitch、有效 I/O 密度和产品级 overlay | SKU datasheet、客户与制造商共同技术披露、同口径 overlay/yield 统计 | 仅称 platform rule / volume-production 状态 |
| U03 | 200 nm test vehicle 是否已转为可售产品或跨客户量产 | 产品公告、可验证技术白皮书、连续批量/收入与可靠性数据 | 保持 A3 test vehicle 标签 |
| U04 | 一致的实际互连密度定义 | grid、pad geometry、fill、有效连接数、routing/yield、面积定义齐全 | 只做 A6 名义格点换算 |
| U05 | 工厂级 post-bond overlay 分布 | wafer/lot/tool/product 分层的 mean、3σ/P99、sample size、pre/post-bond 定义 | 不用“最小值”做横向排名 |
| U06 | 量产 hybrid-bond yield、void/defect、Cu recess 与可靠性 | 缺陷定义、检出限、样本量、WAT/chain、可靠性应力与失效准则 | 不推导良品、成本或有效产能 |
| U07 | traditional TSV、HBM TSV 与 TDV/nTSV 的可比性 | via 类型、深宽比、材料、层级、连接对象和可靠性/产品状态 | TDV/nTSV 单列 |
| U08 | 设备规格到终端产品的映射 | 客户验收、工具配置、相关计量和产品交付证据 | 工具页面不换算为 die 数或市场份额 |
| U09 | Hybrid Bonding 与 HBM4/4E、国内具体项目或算苗 SKU 的工艺关系 | 具名客户/制造/封测联合声明、截面或 flow、datasheet、量产交付 | HBM、TSV/TCB、direct HB 分开建模 |
| U10 | D2W 与 W2W 的 placement/overlay/throughput/OEE 可比数据 | 分别披露模式、KGD、吞吐/OEE 和统计条件 | 不用 W2W 结果代表 D2W |
| U11 | 逻辑-缓存、CIS、NAND、HBM/DRAM 的可靠性和成本窗口 | 具名产品架构、qualification、成本/ASP 或量产节点 | 不以同一 pitch 推导采用速度 |
| U12 | 统一的产能单位 | WSPM、bonded pair、good die、stack、package 的分母、yield、utilization 和周期 | 不相除、不可相加 |
| U13 | 中国本土公开的数字化 pitch/overlay/reliability 资料 | 厂商公开手册、论文、客户联合公告或标准测试报告 | 不用受限设计规则补缺 |

## 硬性门槛

在将 HB/TSV 精度或密度写入产能、销量、市场份额或收入模型之前，以下五项必须同时闭环：

1. **来源与对象：** 公司、结构、W2W/D2W、产品或 test vehicle、晶圆尺寸和时间点明确；
2. **指标口径：** pitch 与 via/pad 定义、pre/post-bond、统计量和样本范围明确；
3. **商业状态：** 若称量产/出货，必须有 SKU、客户/验收或法定财务/交付证据；
4. **可靠性：** 若估算 yield/cost，必须有缺陷、连通与可靠性条件及失效准则；
5. **可比性：** 层级、模式、材料、工艺状态和统计口径相同。

## 取证优先级

1. 制造商与客户联合披露的产品、接口层和交付证据；
2. conference paper / institutional release 的 measurement appendix（保留 wafer size、die coverage、3σ/mean/P99 和可靠性条件）；
3. 设备正式 datasheet 中带单位、条件和对象的规格；
4. TSV 按 traditional TSV、nanoTSV、TDV、backside contact、interposer TSV 独立建表；
5. 只有 A1 出货/收入或明确产品周期被披露后，才把具体工艺渗透率作为市场模型量化输入。
