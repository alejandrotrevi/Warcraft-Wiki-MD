# API UnitHealthMax

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the maximum health of the unit.
 maxHealth = UnitHealthMax(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;maxHealth:{{apitype|number}} - Returns <code>0</code> if the unit does not exist.

==Details==
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|UNIT_MAXHEALTH}} }}
{{apirow | Available after | {{api|t=e|PLAYER_ENTERING_WORLD}} (on login) }}
|}

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 3.0.2|note=Returns absolute health instead of percentages for non party/raid units.}}

====<font color="#4ec9b0">Classic</font>====
* {{Patch 1.13.3|note=Returns absolute health values for NPCs to alleviate addon comms load from the [https://www.curseforge.com/wow/addons/real-mob-health Real Mob Health] addon. Still returns health percentages for players. <small>(Hotfix during build 33302, Feb 7 2020)</small> <ref>{{ref web|url=https://us.forums.blizzard.com/en/wow/t/wow-classic-ui-api-change-for-unithealth/446596|author=Kaivax|date=2020-02-18|title=UI API Change for UnitHealth}}</ref>}}
* {{Patch 1.13.2|note=Added. Shows health percentages for non party/raid units.}}

==References==
```