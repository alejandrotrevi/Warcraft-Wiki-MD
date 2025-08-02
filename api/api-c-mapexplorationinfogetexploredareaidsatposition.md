# API C MapExplorationInfo.GetExploredAreaIDsAtPosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MapExplorationInfo|system=MapExplorationInfo}}
Returns the explored areas for the location on a map.
 areaID = C_MapExplorationInfo.GetExploredAreaIDsAtPosition(uiMapID, normalizedPosition)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]
:;normalizedPosition:{{apitype|Vector2DMixin}}

==Returns==
:;areaID:{{apitype|number[]?}} - {{dbc|areatable|AreaTable.db2}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```