[<< 返回中文主页](README_CN.md)
# 逻辑蓝图的公开电子表格

当电子表格有问题或想提交Pull Request时请在Discord上联系SByte#7574

<!-- TODO: Automate this with actions and json -->
<!-- 前情提要https://docs.google.com/spreadsheets/d/1LQXT5KLEAX0OmkofKDUdt6xcSattJKX6_A9beSJ1A7w/edit#gid=0 -->

| 名称 | 描述 | 作者 | 蓝图链接 | 源码 | 版本 | 最后更新 |
| :--- | --- | --- | :---: | :---: | :--- | ---: |
| CCAD Recon. Control |	payEnter魔法 (有能人给我一个更好的描述吗) |	Cirrocco | [Main Discord](https://discord.com/channels/391020510269669376/640604827344306207/961263533859962912) | | v3a28 | 2022/04/06
| CCER GP Reactor Controller | **反应堆控制器** <br> 通用反应堆控制器 <br><br>- 自启动钍反应堆. <br>- 基于输入功率、系统负载、电池存储的电力和超速效果确定最佳启动时间. <br>- 当电力足够时会启动超速穹顶投影器. <br>- 脑裂功能让你可以在一个大型发电厂中用多个控制器控制不同的反应堆. 只需将所有控制器链接到同一个内存元即可. | Cirrocco | [Main Discord](https://discord.com/channels/391020510269669376/422855426242248725/934609395063595030) | | v5.28 | |
| CCMR Mining Brane | | Cirrocco | [Main Discord](https://discord.com/channels/391020510269669376/640604827344306207/944295882470326425) | | v4.17 | 2022/02/19  |
| Factory Performance | **工厂性能测量逻辑** <br><br>链接单个工厂或重构厂, 或对每个原料蓝图中的工厂进行测试以获得平均的整体性能.<br>- 工厂首次开工后会自动开始计数.<br>- 会报告它测量的时间, 以及它生产单位的时间百分比.<br>- 如果构建因资源不足而暂停, 则会被捕获.<br>当测量单位时, 工厂允许0.4秒的缓冲完成一个单位, 然后开始下一个单位.<br>(全量生产时，爬虫将占96%, t5约为100%)" | Cirrocco | [Main Discord](https://discord.com/channels/391020510269669376/422855426242248725/923309808336125985) | | v2.1 | 2021/12/23 |
| Ratios | **比例计算器** | Bidun | [Main Discord](https://discord.com/channels/391020510269669376/422855426242248725/970050118835396620) | | v1.6 | 2022/05/01 |
| Supply Crew | **通用物品交付** | SBytes | [Main Discord](https://discord.com/channels/391020510269669376/878022862915653723/974570618668318763) | | v2.6.3 | 20220/05/13 |
| uBindFew | 绑定多个单位以添加自己的代码 | Nester | | [Main Discord](https://discord.com/channels/391020510269669376/742769933926269069/902996482599297125) | v2.02 | |
| Ultimate Dome Loader | **基础超速单位补给** | Highfire1 | [Main Discord](https://discord.com/channels/391020510269669376/878022862915653723/925648746870620182) | | v6 |2021/12/29 |
| UMiner Group | **非主控式5单位挖矿**<br>- 表现得像独影AI, 效率高<br>- 挖掘更多的矿石, 例如: 煤炭、沙子、钛和废料<br>- 在挖掘其他矿石之前会挖掘信息表上列出的重要矿石.<br>- 矿石不存在时会自动切换另一个矿石挖掘<br>- 基于存储的资源均匀分配<br>- 高度可配置性 | Username | [Main Discord](https://discord.com/channels/391020510269669376/640604827344306207/942284761827778622) | | v5.2 | 2022/01/31 |
| Smart POD | **智能布超速**<br>当核心内的相位织物超过100但范围内没有小超速时, 将布发送到范围中的大超速中<br>- 探测被链接的方块, 附近有大超速的超速效果时会禁用被链接的小超速<br>- 也可以链接到一个大超速代替小超速 | Gewi | | [Github](https://github.com/Gewi413/mindustry-logic/blob/main/overdrive/normal.mlog) | | 2022/03/13 |
<!-- | | | | | | | | -->

