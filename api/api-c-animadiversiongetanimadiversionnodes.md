# API C AnimaDiversion.GetAnimaDiversionNodes

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AnimaDiversion|system=AnimaDiversionInfo}}
Returns all [[Anima Conductor]] nodes for the player's Covenant.
 animaNodes = C_AnimaDiversion.GetAnimaDiversionNodes()

==Returns==
:;animaNodes:{{apitype|AnimaDiversionNodeInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| talentID || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| costs || {{apitype|AnimaDiversionCostInfo[]}} || 
|-
| currencyID || {{apitype|number}} || 
|-
| icon || {{apitype|number}} || 
|-
| normalizedPosition || {{apitype|Vector2DMixin}} || 
|-
| state || {{apitype|Enum.AnimaDiversionNodeState}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ AnimaDiversionCostInfo
! Field !! Type !! Description
|-
| currencyID || {{apitype|number}} || 
|-
| quantity || {{apitype|number}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ Enum.AnimaDiversionNodeState
! Value !! Field !! Description
|-
| align="center" | 0 || Unavailable || 
|-
| align="center" | 1 || Available || 
|-
| align="center" | 2 || SelectedTemporary || 
|-
| align="center" | 3 || SelectedPermanent || 
|-
| align="center" | 4 || Cooldown || 
|}

==Details==
* Requires interacting with an Anima Conductor at least once since logging on; otherwise, returns nil.  Subsequent calls to {{api|C_UI.Reload()}} will not interrupt this function.

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```