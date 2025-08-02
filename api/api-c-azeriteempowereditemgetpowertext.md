# API C AzeriteEmpoweredItem.GetPowerText

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 powerText = C_AzeriteEmpoweredItem.GetPowerText(azeriteEmpoweredItemLocation, powerID, level)

==Arguments==
:;azeriteEmpoweredItemLocation:{{apitype|ItemLocationMixin}}
:;powerID:{{apitype|number}}
:;level:Enum.AzeritePowerLevel

{| class="sortable darktable zebra"
|-
! Value !! Field !! Description
|-
| <center>0</center> || Base ||
|-
| <center>1</center> || Upgraded ||
|-
| <center>2</center> || Downgraded ||
|}

==Returns==
:;powerText:structure - AzeriteEmpoweredItemPowerText

{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| name || {{apitype|string}} ||
|-
| description || {{apitype|string}} ||
|}

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```