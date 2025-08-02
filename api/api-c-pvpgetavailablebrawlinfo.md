# API C PvP.GetAvailableBrawlInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PvP|system=PvpInfo}}
Needs summary.
 brawlInfo = C_PvP.GetAvailableBrawlInfo()

==Returns==
:;brawlInfo:{{apitype|PvpBrawlInfo?}}
{{:Struct PvpBrawlInfo|nocaption=1}}

==Details==
* If nil is returned, {{api|t=e|PVP_BRAWL_INFO_UPDATED}} event will be sent when the data is ready.

==Patch changes==
* {{Patch 8.1.5|note=Moved to <code>C_PvP.GetAvailableBrawlInfo()</code><sup>[https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_5.lua#26]</sup>}}
* {{Patch 7.2.0|note=Added as <code>C_PvP.GetBrawlInfo()</code>}}
```