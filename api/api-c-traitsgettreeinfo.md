# API C Traits.GetTreeInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Needs summary.
 treeInfo = C_Traits.GetTreeInfo(configID, treeID)

==Arguments==
:;configID:{{apitype|number}}
:;treeID:{{apitype|number}}

==Returns==
:;treeInfo:{{apitype|TraitTreeInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| ID || {{apitype|number}} || 
|-
| gates || {{apitype|TraitGateInfo[]}} || 
|-
| hideSingleRankNumbers || {{apitype|boolean}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ TraitGateInfo
! Field !! Type !! Description
|-
| topLeftNodeID || {{apitype|number}} || 
|-
| conditionID || {{apitype|number}} || 
|}

{{apinavbox|C_Traits}}
```