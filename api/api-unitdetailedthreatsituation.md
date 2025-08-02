# API UnitDetailedThreatSituation

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns detailed info for the threat status of one unit against another.
 isTanking, status, scaledPercentage, rawPercentage, rawThreat = UnitDetailedThreatSituation(unit, mobGUID)

==Arguments==
:;unit:{{apitype|UnitToken}} - The player or pet whose threat to request.
:;mobGUID:{{apitype|UnitToken}} - The NPC whose threat table to query.

==Returns==
:;isTanking:{{apitype|boolean}} - Returns <code>true</code> if the unit is the primary threat target of the '''mobUnit''', returns <code>false</code> otherwise.
:;status:{{apitype|number}} - Threat status of the unit on the '''mobUnit'''.
:;scaledPercentage:{{apitype|number}} - The unit's threat percentage against '''mobUnit'''. At 100% the unit will become the primary target. This value is also scaled the closer the unit is to the mobUnit.
:;rawPercentage:{{apitype|number}} - The unit's threat percentage against '''mobUnit''' relative to the threat of mobUnit's primary target. Can be greater than 100, up to 255. Stops updating when you become the primary target.
:;threatValue:{{apitype|number}} - The unit's total threat value on the '''mobUnit'''.


{{:API_UnitThreatSituation|caption=status}}

==Details==
* ''From wowprogramming.com's API reference:''<ref>http://wowprogramming.com/docs/api/UnitDetailedThreatSituation.html</ref>
<blockquote>"The different values returned by this function reflect the complexity of NPC threat management:

Raw threat roughly equates to the amount of damage a unit has caused to the NPC plus the amount of healing the unit has performed in the NPC's presence. (Each quantity that goes into this sum may be modified, however; such as by a paladin's [[Righteous Fury]] self-buff, a priest's [[Silent Resolve]] talent, or a player whose cloak is enchanted with [[Subtlety (enchant)|Subtlety]].)

Generally, whichever unit has the highest raw threat against an NPC becomes its primary target, and raw threat percentage simplifies this comparison.

However, most NPCs are designed to maintain some degree of target focus -- so that they don't rapidly switch targets if, for example, a unit other than the primary target suddenly reaches 101% raw threat. The amount by which a unit must surpass the primary target's threat to become the new primary target varies by distance from the NPC. 

Thus, a scaled percentage value is given to provide clarity. The rawPercent value returned from this function can be greater than 100 (indicating that unit has greater threat against mobUnit than mobUnit's primary target, and is thus in danger of becoming the primary target), but the scaledPercent value will always be 100 or lower.
	
Threat information for a pair of unit and mobUnit is only returned if the unit has threat against the mobUnit in question. In addition, no threat data is provided if a unit's pet is attacking an NPC but the unit himself has taken no action, even though the pet has threat against the NPC.)"</blockquote>

* When mobs are socially pulled (i.e. they aggro indirectly, as a result of another nearby mob being pulled), 'status' often sets to 0 instead of 3, despite the player having aggro.

==Example==
 /dump UnitDetailedThreatSituation("player", "target")
You have 100% threat on the targeted NPC.
 > true, 3, 100, 100, 15
You have partial threat on the targeted NPC: 66% threat on the mobUnit, 73% threat relative to the primary  target, threat value amount of 25.
 > false, 0, 66.363632202148, 73, 25

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 4.0.3|note=Now returns 0 threat for temporary threat reduction effects like [[Mirror Image]] or [[Fade]] instead of the real value.}}
* {{Patch 3.0.2|note=Added}}

====<font color="#4ec9b0">Classic</font>====
* {{Patch 1.13.5|note=Added.<ref name="1.13.5">{{ref web|url=https://us.forums.blizzard.com/en/wow/t/ptr-patch-notes-wow-classic-version-1135/553585|author=[[Kaivax]]|date=2020-06-12|title=PTR Patch Notes - WoW Classic Version 1.13.5}}</ref>}}

==See also==
* {{api|UnitThreatSituation}}()
* {{api|GetThreatStatusColor}}()
* {{api|t=e|UNIT_THREAT_SITUATION_UPDATE}}
* {{api|t=e|UNIT_THREAT_LIST_UPDATE}}
* {{api|t=c|threatShowNumeric}}

==External links==
{{Elink|type=wowhead|link=https://classic.wowhead.com/guides/threat-overview-classic-wow|desc=Classic WoW Threat Guide by Ragorism}}

==References==
{{reflist}}
```