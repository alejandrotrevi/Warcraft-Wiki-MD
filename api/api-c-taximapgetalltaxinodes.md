# API C TaxiMap.GetAllTaxiNodes

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TaxiMap|system=TaxiMap}}
Returns information on taxi nodes at the current flight master.
 taxiNodes = C_TaxiMap.GetAllTaxiNodes(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}} : [[UiMapID]]

==Returns==
:;taxiNodes:{{apitype|TaxiNodeInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| nodeID || {{apitype|number}} || 
|-
| position || {{apitype|vector2}} || 
|-
| name || {{apitype|string}} || 
|-
| state || {{apitype|Enum.FlightPathState}} || 
|-
| slotIndex || {{apitype|number}} || 
|-
| textureKit || {{apitype|textureKit}} || 
|-
| useSpecialIcon || {{apitype|boolean}} || 
|-
| specialIconCostString || {{apitype|string?}} || 
|-
| isMapLayerTransition || {{apitype|boolean}} || <font color="green">10.1.0</font>
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.FlightPathState
! Value !! Field !! Description
|-
| 0 || Current || 
|-
| 1 || Reachable || 
|-
| 2 || Unreachable || 
|}

==Patch changes==
* {{Patch 9.2.0|note=Added <code>useSpecialIcon, specialIconCostString</code> fields.}}
* {{Patch 8.1.0|note=Added <code>uiMapID</code> argument.}}
* {{Patch 8.0.1|note=Moved to <code>C_TaxiMap.GetAllTaxiNodes()</code>}}
* {{Patch 7.0.3|note=Added as <code>GetAllTaxiNodes()</code>}}
```