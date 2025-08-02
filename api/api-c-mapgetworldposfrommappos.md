# API C Map.GetWorldPosFromMapPos

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Translates a map position to a world map position.
 continentID, worldPosition = C_Map.GetWorldPosFromMapPos(uiMapID, mapPosition)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]
:;mapPosition:{{apitype|Vector2DMixin}} - as returned from {{api|C_Map.GetPlayerMapPosition}}()

==Returns==
:;continentID:{{apitype|number}} : [[InstanceID]]
:;worldPosition:{{apitype|Vector2DMixin}}

==Example==
Prints the world coords and size for the boundary box of Elwynn Forest.
<syntaxhighlight lang="lua">
/dump C_Map.GetWorldPosFromMapPos(37, {x=0, y=0}) -- x = -7939.580078125, y = 1535.4200439453
/dump C_Map.GetWorldPosFromMapPos(37, {x=1, y=1}) -- x = -10254.200195312, y = -1935.4200439453
/dump C_Map.GetMapWorldSize(37) -- 3470.8400878906, 2314.6201171875
</syntaxhighlight>


Returns the [[https://warcraft.wiki.gg/wiki/InstanceID#Zones Continent ID]] of player as well as the worldPos x, y coordinates

 /run local mapID = C_Map.GetBestMapForUnit("player") local pos = C_Map.GetPlayerMapPosition(mapID, "player") local continentID, worldPos = C_Map.GetWorldPosFromMapPos(mapID, pos) print("Continent ID:", continentID, "World Position:", "x =", worldPos.x, "y =", worldPos.y)

==Patch changes==
* {{Patch 8.0.1|note=Added.}}

==See also==
* {{api|UnitPosition}}()
* [https://www.wowace.com/projects/herebedragons HereBeDragons] library
```