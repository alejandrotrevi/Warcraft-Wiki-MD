# API C Map.GetMapArtHelpTextPosition

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns the position for the "Click to Zoom In" hint text on flight maps.
 position = C_Map.GetMapArtHelpTextPosition(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;position:{{apitype|Enum.MapCanvasPosition}}
{{:Enum.MapCanvasPosition|nocaption=1}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```