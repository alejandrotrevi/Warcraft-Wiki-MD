# API C CovenantSanctumUI.GetRenownRewardsForLevel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CovenantSanctumUI|system=CovenantSanctumUI}}
Needs summary.
 rewards = C_CovenantSanctumUI.GetRenownRewardsForLevel(covenantID, renownLevel)

==Arguments==
:;covenantID:{{apitype|Enum.CovenantType}}
{{:Enum.CovenantType|nocaption=1}}
:;renownLevel:{{apitype|number}}

==Returns==
:;rewards:{{apitype|CovenantSanctumRenownRewardInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| uiOrder || {{apitype|number}} || 
|-
| itemID || {{apitype|number?}} || 
|-
| spellID || {{apitype|number?}} || 
|-
| mountID || {{apitype|number?}} || 
|-
| transmogID || {{apitype|number?}} || 
|-
| transmogSetID || {{apitype|number?}} || 
|-
| titleMaskID || {{apitype|number?}} || <font color="green">9.0.2</font>
|-
| garrFollowerID || {{apitype|number?}} || 
|-
| transmogIllusionSourceID || {{apitype|number?}} || 
|-
| icon || {{apitype|number?}} || 
|-
| name || {{apitype|string?}} || 
|-
| description || {{apitype|string?}} || 
|-
| toastDescription || {{apitype|string?}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```