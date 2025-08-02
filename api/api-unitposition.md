# API UnitPosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}} {{restrictedapi|noinstance}}
Returns the position of a unit in the current world area.
 positionX, positionY, positionZ, mapID = UnitPosition(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit for which the position is returned. Does not work with all unit types. Works with <code>"player"</code>, <code>"party''N''"</code> or <code>"raid''N''"</code> as unit type. In particular, it does not work on pets or any unit not in your group.

==Returns==
:;positionX:{{apitype|number}} - Y value of the unit's position in yards, relative to the instance
:;positionY:{{apitype|number}} - X value of the unit's position in yards, relative to the instance
:;positionZ:{{apitype|number}} - Always 0. A placeholder for the Z coordinate
:;mapID:{{apitype|number}} : [[InstanceID]]

==Example==
Returns the distance in yards between 2 units in the same raid, or nil if they're not in the same instance or are in a raid/dungeon/competitive instance.
 function ComputeDistance(unit1, unit2)
   local y1, x1, _, instance1 = UnitPosition(unit1)
   local y2, x2, _, instance2 = UnitPosition(unit2)
   return instance1 == instance2 and ((x2 - x1) ^ 2 + (y2 - y1) ^ 2) ^ 0.5
 end

It's important to note that since this number is being measured from the '''center''' of the two units, and spell ranges are calculated from the edge of their hitbox, you will need to subtract 3 yards if you're using this function for measuring spell distance between players.

==Patch changes==
* {{Patch 7.1.0|note=Returns nil while inside a restricted area (instance/battleground/arena).<sup>[http://www.mmo-champion.com/content/5921-Gamescom-Developer-Interview-Addon-Changes-in-Patch-7-1][http://www.wowhead.com/news=255220/gamescom-interview-with-ion-watcher-hazzikostas-and-slootbag][https://twitter.com/deadlybossmods/status/767097033995849728]</sup>}}
* {{Patch 6.0.2|note=Added.}}
```