# API C LegendaryCrafting.GetRuneforgeItemPreviewInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LegendaryCrafting|system=LegendaryCrafting}}
Needs summary.
 info = C_LegendaryCrafting.GetRuneforgeItemPreviewInfo(baseItem [, runeforgePowerID, modifiers])

==Arguments==
:;baseItem:{{apitype|ItemLocationMixin}}
:;runeforgePowerID:{{apitype|number?}}
:;modifiers:{{apitype|number[]?}}

==Returns==
:;info:{{apitype|RuneforgeItemPreviewInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| itemGUID || {{apitype|string}} || 
|-
| itemLevel || {{apitype|number}} || 
|-
| itemName || {{apitype|string}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```