# API C Container.GetContainerItemPurchaseItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Container|system=Container}}
Needs summary.
 itemInfo = C_Container.GetContainerItemPurchaseItem(containerIndex, slotIndex, itemIndex, isEquipped)

==Arguments==
:;containerIndex:{{apitype|number}}
:;slotIndex:{{apitype|number}}
:;itemIndex:{{apitype|number}}
:;isEquipped:{{apitype|boolean}}

==Returns==
:;itemInfo:{{apitype|ItemPurchaseItem}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| iconFileID || {{apitype|number?}} || 
|-
| itemCount || {{apitype|number}} || 
|-
| hyperlink || {{apitype|string}} || 
|}
```