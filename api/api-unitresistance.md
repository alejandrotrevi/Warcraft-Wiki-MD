# API UnitResistance

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets information about a unit's resistance.
 base, total, bonus, minus = UnitResistance(unit [, resistanceIndex])

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit to check
:;resistanceIndex:{{apitype|number}} - The index of the resistance type to check
:;:* 0 - (Physical) - Armor rating
:;:* 1 - (Holy) 
:;:* 2 - (Fire)
:;:* 3 - (Nature) 
:;:* 4 - (Frost) 
:;:* 5 - (Shadow) 
:;:* 6 - (Arcane) 

==Returns==
:;base:{{apitype|number}} - The base resistance
:;total:{{apitype|number}} - The current total value after all modifiers
:;bonus:{{apitype|number}} - The bonus resistance modifier total from gear and buffs
:;minus:{{apitype|number}} - The negative resistance modifier total from gear and buffs

==Example==
 /script SendChatMessage("My base armor is ".. UnitResistance("player", 0));

 /script _, total, _, _ = UnitResistance("player",0)); SendChatMessage("My total armor is "..total);

==Patch changes==
* {{Patch 8.0.1|note=Removed.}}
```