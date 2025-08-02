# API C Garrison.GetTalentTreeInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Garrison|system=GarrisonInfo}}
Needs summary.
 info = C_Garrison.GetTalentTreeInfo(treeID)

==Arguments==
:;treeID:{{apitype|number}}

==Returns==
:;info:{{apitype|GarrisonTalentTreeInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| treeID || {{apitype|number}} || 
|-
| title || {{apitype|string}} || 
|-
| textureKit || {{apitype|string}} || 
|-
| talents || {{apitype|GarrisonTalentInfo[]}} || 
|-
| isClassAgnostic || {{apitype|boolean}} || 
|-
| isThemed || {{apitype|boolean}} || 
|-
| featureType || {{apitype|number}} || 
|-
| featureSubtype || {{apitype|number}} || 
|}

{{:Struct GarrisonTalentInfo}}
```