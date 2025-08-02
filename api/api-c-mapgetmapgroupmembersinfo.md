# API C Map.GetMapGroupMembersInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Map|system=MapUI}}
Returns the floors for a map group.
 info = C_Map.GetMapGroupMembersInfo(uiMapGroupID)

==Arguments==
:;uiMapGroupID:{{apitype|number}}

==Returns==
:;info:{{apitype|table}} UiMapGroupMemberInfo[]
{| class="sortable darktable zebra" style="margin-left: 3.9em"
<!-- |+ [[Struct Map.UiMapGroupMemberInfo|UiMapGroupMemberInfo]] -->
! Field !! Type !! Description
|-
| mapID || {{apitype|number}} || [[UiMapID]]
|-
| relativeHeightIndex || {{apitype|number}} ||
|-
| name || {{apitype|string}} || Floor name
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```