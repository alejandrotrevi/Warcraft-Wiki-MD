# API UnitThreatPercentageOfLead

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Needs summary.
 percentage = UnitThreatPercentageOfLead(unit, mobGUID)

==Arguments==
:;unit:{{apitype|UnitToken}} - The player or pet whose threat to request.
:;mobGUID:{{apitype|UnitToken}} - The NPC whose threat table to query.

==Returns==
:;percentage:{{apitype|number}}

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 4.1.0|note=Added.<ref>{{Ref FrameXML|UnitFrame.lua|version=4.1.0|line=516|diff=}}</ref>}}

====<font color="#4ec9b0">Classic</font>====
* {{Patch 1.13.5|note=Added.<ref>{{ref web|url=https://us.forums.blizzard.com/en/wow/t/ptr-patch-notes-wow-classic-version-1135/553585|author=[[Kaivax]]|date=2020-06-12|title=PTR Patch Notes - WoW Classic Version 1.13.5}}</ref>}}

==See also==
* {{api|UnitDetailedThreatSituation}}()
* {{api|t=c|threatShowNumeric}}

==References==
{{reflist}}
```