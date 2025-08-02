# API C Map.GetMapInfoAtPosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns info for any child or adjacent maps at a position on the map.
 info = C_Map.GetMapInfoAtPosition(uiMapID, x, y [, ignoreZoneMapPositionData])

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]
:;x:{{apitype|number}} : [0.0 - 1.0]
:;y:{{apitype|number}} : [0.0 - 1.0]
:;ignoreZoneMapPositionData:{{apitype|boolean?}}

==Returns==
:;info:{{apitype|UiMapDetails}}
{{:Struct UiMapDetails|nocaption=1}}

==Details==
* No return value in instances, the WoD Garrison, the beginning of the new player experience, or empty regions of the cosmic map.
* Otherwise, returns map info for:
** Child maps, such as zones in a continent.
** Adjacent maps, such as zones next to the current one.
** The current map, similar to {{api|C_Map.GetMapInfo()}}.

==Patch changes==
* {{Patch 10.1.0|note=Added <code>ignoreZoneMapPositionData</code> argument.}}
* {{Patch 8.0.1|note=Added.}}
```