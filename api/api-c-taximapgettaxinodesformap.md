# API C TaxiMap.GetTaxiNodesForMap

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TaxiMap|system=TaxiMap}}
Returns information on taxi nodes for a given map, without considering the current flight master.
 mapTaxiNodes = C_TaxiMap.GetTaxiNodesForMap(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;mapTaxiNodes:{{apitype|MapTaxiNodeInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|nodeID}} || {{apitype|number}} || 
|-
| {{apiname|position}} || {{apitype|vector2}} || 
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|atlasName}} || {{apitype|string}} || [[AtlasID]]
|-
| {{apiname|faction}} || {{apitype|Enum.FlightPathFaction}} || 
|-
| {{apiname|textureKit}} || {{apitype|textureKit}} || 
|-
| {{apiname|isUndiscovered}} || {{apitype|boolean}} || <font color="green">11.0.0</font>
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.FlightPathFaction
! Value !! Field !! Description
|-
| 0 || {{apiname|Neutral}} || 
|-
| 1 || {{apiname|Horde}} || 
|-
| 2 || {{apiname|Alliance}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added <code>textureKit</code> field.}}
* {{Patch 8.0.1|note=Added.}}
```