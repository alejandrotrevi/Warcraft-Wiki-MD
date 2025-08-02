# API C Commentator.GetUnitData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Commentator|system=CommentatorFrame}}
Needs summary.
 data = C_Commentator.GetUnitData(unitToken)

==Arguments==
:;unitToken:{{apitype|string}} : [[UnitId]]

==Returns==
:;data:{{apitype|CommentatorUnitData}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| healthMax || {{apitype|number}} || 
|-
| health || {{apitype|number}} || 
|-
| absorbTotal || {{apitype|number}} || 
|-
| isDeadOrGhost || {{apitype|boolean}} || 
|-
| isFeignDeath || {{apitype|boolean}} || 
|-
| powerTypeToken || {{apitype|string}} || 
|-
| power || {{apitype|number}} || 
|-
| powerMax || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```