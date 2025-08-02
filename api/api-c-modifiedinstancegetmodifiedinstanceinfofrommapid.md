# API C ModifiedInstance.GetModifiedInstanceInfoFromMapID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ModifiedInstance|system=UIModifiedInstance}}
Needs summary.
 info = C_ModifiedInstance.GetModifiedInstanceInfoFromMapID(mapID)

==Arguments==
:;mapID:{{apitype|number}}

==Returns==
:;info:{{apitype|ModifiedInstanceInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| lfrItemLevel || {{apitype|number?}} || 
|-
| normalItemLevel || {{apitype|number?}} || 
|-
| heroicItemLevel || {{apitype|number?}} || 
|-
| mythicItemLevel || {{apitype|number?}} || 
|-
| uiTextureKit || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|}

==Patch changes==
* {{Patch 9.2.5|note=Added.}}
```