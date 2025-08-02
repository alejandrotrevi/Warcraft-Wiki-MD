# API C ReportSystem.CanReportPlayer

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ReportSystem|system=ReportSystem}}
Returns if a player can be reported.
 canReport = C_ReportSystem.CanReportPlayer(playerLocation)

==Arguments==
:;playerLocation:{{apitype|PlayerLocationMixin}}

==Returns==
:;canReport:{{apitype|boolean}}

==Patch changes==
* {{Patch 8.1.5|note=Replaces {{api|C_ChatInfo.CanReportPlayer}}() which is deprecated<sup>[https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#210]</sup>}}
* {{Patch 8.1.0|note=Added.}}
```