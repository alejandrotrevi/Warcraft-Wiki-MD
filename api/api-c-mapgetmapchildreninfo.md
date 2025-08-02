# API C Map.GetMapChildrenInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns info for the children of a map.
 info = C_Map.GetMapChildrenInfo(uiMapID [, mapType, allDescendants])

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]
:;mapType:{{apitype|Enum.UIMapType?}}  - Filters results by a specific map type.
:;allDescendants:{{apitype|boolean?}}  - Whether to recurse on each child or not.

==Returns==
:;info:{{apitype|UiMapDetails[]}}
{{:Struct Map.UiMapDetails|nocaption=1}}

==Example==
* Children of the "Cosmic" uiMapID (not to be confused with the UIMapType).
 /dump C_Map.GetMapChildrenInfo(946)

 {
 	{mapType=2, mapID=101, name="Outland", parentMapID=946},
 	{mapType=2, mapID=572, name="Draenor", parentMapID=946},
 	{mapType=1, mapID=947, name="Azeroth", parentMapID=946}
 }

* Children of the "Cosmic" uiMapID with mapType==2
 /dump C_Map.GetMapChildrenInfo(946, 2)

 {
 	{mapType=2, mapID=101, name="Outland", parentMapID=946},
 	{mapType=2, mapID=572, name="Draenor", parentMapID=946}
 }

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```