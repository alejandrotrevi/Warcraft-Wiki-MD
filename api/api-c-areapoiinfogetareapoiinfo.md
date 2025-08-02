# API C AreaPoiInfo.GetAreaPOIInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an area point of interest (e.g. World PvP objectives).

 poiInfo = C_AreaPoiInfo.GetAreaPOIInfo([uiMapID], areaPoiID)

==Arguments==
:;uiMapID:{{apitype|number?}} : [[UiMapID]] - When omitted this appears to default to the relevant ui map id, regardless of the player's current location or any ui map being viewed.
:;areaPoiID:{{apitype|number}} : {{dbc|areapoi|AreaPOI}}

==Returns==
[[File:POIIcons.png|thumb|POIIcons]]
:;poiInfo:{{apitype|AreaPOIInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|areaPoiID}} || {{apitype|number}} || 
|-
| {{apiname|position}} || {{apitype|vector2}} || 
|-
| {{apiname|name}} || {{apitype|string}} || e.g. "Domination Point Tower"
|-
| {{apiname|description}} || {{apitype|string?}} || e.g. "Horde Controlled" or "Grand Master Pet Tamer"
|-
| {{apiname|linkedUiMapID}} || {{apitype|number?}} || <font color="green">11.0.0</font>
|-
| {{apiname|textureIndex}} || {{apitype|number?}} || 
|-
| {{apiname|tooltipWidgetSet}} || {{apitype|number?}} || <font color="green">10.2.6</font> - Renamed from <code>widgetSetID</code><br>ID for {{api|t=a|C_UIWidgetManager.GetAllWidgetsBySetID}}
|-
| {{apiname|iconWidgetSet}} || {{apitype|number?}} || <font color="green">10.2.6</font>
|-
| {{apiname|atlasName}} || {{apitype|string?}} || [[AtlasID]]
|-
| {{apiname|uiTextureKit}} || {{apitype|textureKit?}} || <font color="green">9.0.1</font>
|-
| {{apiname|shouldGlow}} || {{apitype|boolean}} || <font color="green">9.0.5</font>
|-
| {{apiname|factionID}} || {{apitype|number?}} || <font color="green">10.0.2</font>
|-
| {{apiname|isPrimaryMapForPOI}} || {{apitype|boolean}} || <font color="green">10.0.2</font>
|-
| {{apiname|isAlwaysOnFlightmap}} || {{apitype|boolean}} || <font color="green">10.0.2</font>
|-
| {{apiname|addPaddingAboveTooltipWidgets}} || {{apitype|boolean?}} || <font color="green">10.2.6</font> - Renamed from <code>addPaddingAboveWidgets</code>
|-
| {{apiname|highlightWorldQuestsOnHover}} || {{apitype|boolean}} || 
|-
| {{apiname|highlightVignettesOnHover}} || {{apitype|boolean}} || 
|-
| {{apiname|isCurrentEvent}} || {{apitype|boolean}} || <font color="green">11.0.0</font>
|}

==Details==
* The <code>textureIndex</code> specifies an icon from [https://github.com/Gethe/wow-ui-textures/blob/live/MINIMAP/POIICONS.PNG Interface/Minimap/POIIcons]. You can use {{api|GetPOITextureCoords}}() to resolve these indices to texture coordinates. [https://github.com/Gethe/wow-ui-source/blob/c227f01bfe38173b2614d8b65947ab21fd25a839/AddOns/Blizzard_SharedMapDataProviders/SharedMapPoiTemplates.lua#L48]

==Example==
 /dump C_AreaPoiInfo.GetAreaPOIInfo(2339, 7898)

[[File:API_C_AreaPoiInfo.GetAreaPOIInfo.png]] [[File:API_C_AreaPoiInfo.GetAreaPOIInfo_02.png]]

==Patch changes==
* {{Patch 11.1.0|note=<code>uiMapID</code> argument is optional.}}
* {{Patch 8.0.1|note=Added. Replaces {{api|C_WorldMap.GetMapLandmarkInfo}}().}}
```