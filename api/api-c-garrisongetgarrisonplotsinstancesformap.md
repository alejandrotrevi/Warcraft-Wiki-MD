# API C Garrison.GetGarrisonPlotsInstancesForMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 garrisonPlotInstances = C_Garrison.GetGarrisonPlotsInstancesForMap(uiMapID)

==Arguments==
:;[[UiMapID|uiMapID]]:{{apitype|number}}

==Returns==
:;garrisonPlotInstances:structure - GarrisonPlotInstanceMapInfo[]

{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| buildingPlotInstanceID || {{apitype|number}} || 
|-
| position || {{apitype|Vector2DMixin}} || 
|-
| name || {{apitype|string}} || 
|-
| atlasName || {{apitype|string}} || [[AtlasID]] used as {{api|t=w|Texture:SetAtlas(atlasName)}}
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```