# API C Map.GetMapHighlightInfoAtPosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns a map highlight pin for a location.
 fileDataID, atlasID, texturePercentageX, texturePercentageY, textureX, textureY, scrollChildX, scrollChildY = C_Map.GetMapHighlightInfoAtPosition(uiMapID, x, y)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]
:;x:{{apitype|number}}
:;y:{{apitype|number}}

==Returns==
:;fileDataID:{{apitype|number}} - [[FileDataID]]
:;atlasID:{{apitype|string}} - [[AtlasID]]
:;texturePercentageX:{{apitype|number}}
:;texturePercentageY:{{apitype|number}}
:;textureX:{{apitype|number}}
:;textureY:{{apitype|number}}
:;scrollChildX:{{apitype|number}}
:;scrollChildY:{{apitype|number}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```