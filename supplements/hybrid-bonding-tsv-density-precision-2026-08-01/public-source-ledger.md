# 公开来源台账与复核锚点

**读取日期：** 2026-07-31

**规则：** 每条均为企业、设备商或研究机构的公开原始页面。不得把搜索引擎摘要、二手媒体转述、专利标题、设备订单或厂房照片当作本台账的证据本体。

| ID | 公开来源 | 页面内复核锚点 | 分类/等级 | 可证明 | 不能证明 |
|---|---|---|---|---|---|
| P01 | [TSMC-SoIC®](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/SoIC.htm) | `sub-10µm rule`；`volume production in 2025` | 制造商平台 / A2 | SoIC 的公开规则尺度和 3 nm stacking 量产平台状态 | SKU、实际 pitch、overlay、yield、客户、WPM、die 出货 |
| P02 | [EVG®6200∞ BA Automated Bond Alignment System](https://www.evgroup.com/products/bonding/bond-alignment-systems/evg6200-infinity-ba) | `Backside alignment`；`Transparent alignment`；`3 σ` | 工具规格 / A2 | 指定工具的 alignment spec 与 pilot/volume production 定位 | 产品 post-bond overlay、客户装机、成品 yield/出货 |
| P03 | [imec and EVG: 1.8 µm pitch overlay accuracy](https://www.evgroup.com/company/news/detail/imec-and-evg-demonstrate-for-the-first-time-1-8-m-pitch-overlay-accuracy-for-wafer-bonding-1556544424) | `hybrid (via-middle)`；`1.8µm pitch`；`dielectric (via-last)`；`300nm overlay` | 联合研究 / A3 | 不同研究分支各自的 1.8 µm 或 300 nm 记录 | 把 dielectric overlay 归入 hybrid，或量化产品 yield |
| P04 | [Leti: 300 mm W2W direct hybrid bonding with 1 µm pitch](https://www.evgroup.com/company/news/detail/leti-demonstrates-world-s-first-300-mm-wafer-to-wafer-direct-hybrid-bonding-with-1-micron-pitch-on-ev-group-system-1556468468) | `195nm (3-sigma)`；`mean alignment`；`1µm to 4µm` | 研究演示 / A3 | 300 mm W2W 研究结构与对应统计口径 | 客户产品量产、商业出货、跨批次良率 |
| P05 | [imec: W2W hybrid bonding toward 400 nm pitch](https://www.imec-int.com/en/articles/wafer-wafer-hybrid-bonding-pushing-boundaries-400nm-interconnect-pitch) | `400nm pitch`；`overlay below 150nm`；`smaller than 100nm` | 研究更新 / A3 | 400 nm 研究结果与 HVM 所需控制判断 | `<100 nm` 已达成量产 KPI、产品 yield/出货 |
| P06 | [imec: high-density front and backside wafer connectivity](https://www.imec-int.com/en/articles/path-high-density-front-and-backside-wafer-connectivity) | `250nm pitch`；`120nm pitch`；`20nm`；`15nm overlay margin` | 研究/会议成果 / A3 | W2W HB、TDV/nTSV 与 design margin 的特定研究边界 | TDV/nTSV 是所有 TSV，或 15 nm 是实测工具精度 |
| P07 | [imec and EVG: 200 nm HB with record overlay accuracy](https://www.evgroup.com/company/news/detail/imec-and-ev-group-demonstrate-wafer-to-wafer-hybrid-bonding-with-200nm-interconnect-pitch-and-record-high-overlay-accuracy) | `test vehicle`；`200nm`；`below 40nm`；`100% of the dies` | 联合 test vehicle / A3 | 300 mm、全片/所有 die 范围内的公开测试车结果 | 客户产品、商品化批量、A1 出货或量化 yield |
| P08 | [Besi Datacon 8800 CHAMEO ultra plus AC](https://www.besi.com/products-technology/product-details/product/datacon-8800-chameo-ultra-plus-ac/) | `ISO3`；`Inline IR Inspection`；`Demonstrations and sample builds` | 设备能力/样品服务 / A2 | 公开设备能力与演示/样品支持 | 数字化 placement/overlay、客户量产、产品出货 |
| P09 | [Besi Hybrid Bonding product group](https://www.besi.com/products-technology/productgroup/hybrid-bonding/) | `optical alignment`；`high-density interconnects`；`yield` | 设备平台说明 / A2 | 平台级能力描述 | 数字化精度、吞吐、产量或客户商业化 |

## 复核方法

1. 打开表中原始 URL；
2. 使用“页面内复核锚点”查找具体文字；
3. 确认同一页面内的工艺模式（W2W/D2W）、晶圆尺寸、对象（工具、研究结构、test vehicle 或产品平台）和统计口径；
4. 在引用时同时保留“来源主体 + 工艺对象 + 数值 + 证据类型”四项。

正确示例：

> imec 与 EVG 在 2026 年公布的 300 mm **test vehicle** 上报告 200 nm Cu pad pitch 和全片 100% die 的 post-bond overlay vector `<40 nm`（联合研究/ECTC test vehicle，不是产品出货）。[P07]

禁止示例：

> EVG 200 nm 已量产；或 imec 的 40 nm 是所有 HB 设备精度。

## 可比性检查

| 对比问题 | 能否直接比较 | 原因 |
|---|---|---|
| P01 的 sub-10 µm 与 P07 的 200 nm | 否；只可做技术尺度参考 | A2 平台描述与 A3 test vehicle 的对象不同 |
| P02 的 ±1/±2 µm 与 P07 的 `<40 nm` | 否 | 工具对准规格与键合后 pad-to-pad overlay 的定义不同 |
| P03 的 300 nm 与 P04/P05/P07 的 HB overlay | 否 | P03 的 300 nm 属于 dielectric/via-last 分支 |
| P06 的 120 nm TDV/nTSV 与 HB pad pitch | 否 | 背面细连接与 bond pad 的层级、分母和价值链不同 |
| 25% designed Cu density 与 actual I/O/yield | 否 | Cu 面积 fill 不等于有效连接、路由率、电性通过率或产品 yield |
