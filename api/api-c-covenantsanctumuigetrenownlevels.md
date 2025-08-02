# API C CovenantSanctumUI.GetRenownLevels

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CovenantSanctumUI|system=CovenantSanctumUI}}
Needs summary.
 levels = C_CovenantSanctumUI.GetRenownLevels(covenantID)

==Arguments==
:;covenantID:{{apitype|Enum.CovenantType}}
{{:Enum.CovenantType|nocaption=1}}

==Returns==
:;levels:{{apitype|CovenantSanctumRenownLevelInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| level || {{apitype|number}} || 
|-
| locked || {{apitype|boolean}} || 
|-
| isMilestone || {{apitype|boolean}} || 
|-
| isCapstone || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 9.0.2|note=Added.}}
```