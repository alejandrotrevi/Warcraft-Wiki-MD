# API C Map.GetBestMapForUnit

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns the current UI map for the given unit. Only works for the player and group members.
 uiMapID = C_Map.GetBestMapForUnit(unitToken)

==Arguments==
:;unitToken:{{apitype|string}} : [[UnitId]]

==Returns==
:;uiMapID:{{apitype|number?}} : [[UiMapID]] - Returns the "lowest" map the unit is on. For example, if a unit is in a microdungeon it will return that instead of the zone or continent map.

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|C_Map.GetMapInfo}}<br>{{api|GetInstanceInfo}} }}
{{apirow | Related Events | {{api|t=e|ZONE_CHANGED}}<br>{{api|t=e|ZONE_CHANGED_NEW_AREA}} }}
|}

==Example==
<onlyinclude>Prints the current map for the player.
<syntaxhighlight lang="lua">
/run local mapID = C_Map.GetBestMapForUnit("player"); print(format("You are in %s (%d)", C_Map.GetMapInfo(mapID).name, mapID))
-- You are in Stormwind City (84)
</syntaxhighlight></onlyinclude>

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```