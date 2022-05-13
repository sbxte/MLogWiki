[<< return to main page](../README.md)
# Public Spreadsheet of Logic Schemes

Ping SByte#7574 on discord for issues with spreadsheet or submit a pull request.

<!-- TODO: Automate this with actions and json -->
<!-- previously on https://docs.google.com/spreadsheets/d/1LQXT5KLEAX0OmkofKDUdt6xcSattJKX6_A9beSJ1A7w/edit#gid=0 -->

| Name | Description | Author | Schematic Link | Source Code | Version | Last Updated |
| :--- | --- | --- | :---: | :---: | :--- | ---: |
| CCAD Recon. Control |	payEnter magic (someone give me a better description) |	Cirrocco | [Main Discord](https://discord.com/channels/391020510269669376/640604827344306207/961263533859962912) | | v3a28 | 4/6/2022
| CCER GP Reactor Controller | **Reactor Controller** <br> General Purpose Reactor Controller <br><br>- Self-starts thorium reactors. <br>- Determines optimal time to start impacts based on input power, system load, stored battery power, and overdrive influence. <br>- Overdrive will be enabled when sufficient power to do so. <br>- Split-brain function lets you have multiple controllers in a large power plant controlling different reactors. just connect all controllers to the same memcell. | Cirrocco | [Main Discord](https://discord.com/channels/391020510269669376/422855426242248725/934609395063595030) | | v5.28 | |
| CCMR Mining Brane | | Cirrocco | [Main Discord](https://discord.com/channels/391020510269669376/640604827344306207/944295882470326425) | | v4.17 | 2/19/2022  |
| Factory Performance | **Factory Performance Measurement Logic** <br><br>Connect a single factory or reconstructor, or to every factory in a material schem to get average overall performance.<br>- Automatically starts counting after the factory starts work for the first time.<br>- Will report how long it's been measuring, and what percent of the time it's been producing units.<br>- Will catch if a build stalls due to lack of resources.<br>When measuring unit factories allow for a 0.4s buffer to finish a unit, and start the next.<br>(crawler would be 96% for full production, t5 would be about 100%)" | Cirrocco | [Main Discord](https://discord.com/channels/391020510269669376/422855426242248725/923309808336125985) | | v2.1 | 12/23/2021 |
| Ratios | **Ratios Calculator** | Bidun | [Main Discord](https://discord.com/channels/391020510269669376/878022862915653723/939378485317746721) | | v1.53 | 2/5/2022 |
| Supply Crew | **General purpose item delivery** | SBytes | [Main Discord](https://discord.com/channels/391020510269669376/878022862915653723/974570618668318763) | | v2.6.3 | 05/13/2022 |
| uBindFew | Binds multiple units for you to add your own code | Nester | | [Main Discord](https://discord.com/channels/391020510269669376/742769933926269069/902996482599297125) | v2.02 | |
| Ultimate Dome Loader | **Unit based dome feeder** | Highfire1 | [Main Discord](https://discord.com/channels/391020510269669376/878022862915653723/925648746870620182) | | v6 |12/29/2021 |
| UMiner Group | **5 Unit Type Non-controlled miner**<br>- Behave almost like mono ai, high efficiency<br>- Mine more resource type, eg. coal, sand and scrap<br>- Mine important ore first before mine else, listed in message<br>- Change mine ore automaticly if the ore not exist<br>- Evenly distributed based the res stored<br>- Highly configurable | Username | [Main Discord](https://discord.com/channels/391020510269669376/640604827344306207/942284761827778622) | | v5.2 | 1/31/2022 |
| Smart POD | **Smart Phase Overdrive**<br>Sends phase into an overdrive when there is more than 100 in core but no dome in range<br>- Link to projector/dome, probe points that need to be under dome to disable<br>- Can also be linked to a dome to supply it instead of the projector | Gewi | | [Github](https://github.com/Gewi413/mindustry-logic/blob/main/overdrive/normal.mlog) | | 3/13/2022 |
<!-- | | | | | | | | -->

