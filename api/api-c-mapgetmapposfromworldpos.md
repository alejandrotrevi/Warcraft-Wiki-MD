# API C Map.GetMapPosFromWorldPos

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Translates a world map position to a map position.
 uiMapID, mapPosition = C_Map.GetMapPosFromWorldPos(continentID, worldPosition [, overrideUiMapID])

==Arguments==
:;continentID:{{apitype|number}} - [[InstanceID]] of the continent
:;worldPosition:{{apitype|Vector2DMixin}}
:;overrideUiMapID:{{apitype|number?}} - If you don't set this to the map that you want a relative position in, it defaults to the mapID for the player's continent, essentially normalizing world coordinates (i.e. 478.1,598.2) into continent map coordinates (i.e. 0.44,0.61)

==Returns==
:;uiMapID:{{apitype|number}} : [[UiMapID]]
:;mapPosition:{{apitype|Vector2DMixin}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```