# API C Map.GetBountySetMaps

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns the maps for a bounty.
 mapIDs = C_Map.GetBountySetMaps(bountySetID)

==Arguments==
:;bountySetID:{{apitype|number}} - from {{dbc|bountyset|BountySet.db2}}

==Returns==
:;mapIDs:{{apitype|number[]}} : [[UiMapID]]

==Values==
* List of Bounty IDs and their UiMap IDs.
{| class="sortable darktable zebra"
|-
! ID !! UiMapIDs
|-
| <center>4</center> || 627, 630, 634, 641, 646, 650, 680, 739, 790, 830, 882, 885
|-
| <center>10</center> || 14, 862, 863, 864, 875, 876, 895, 896, 942, 1161, 1165, 1193, 1194, 1195, 1196, 1197, 1198, 62
|}

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```