# API C Container.GetContainerItemPurchaseCurrency

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Container|system=Container}}
Needs summary.
 currencyInfo = C_Container.GetContainerItemPurchaseCurrency(containerIndex, slotIndex, itemIndex, isEquipped)

==Arguments==
:;containerIndex:{{apitype|number}}
:;slotIndex:{{apitype|number}}
:;itemIndex:{{apitype|number}}
:;isEquipped:{{apitype|boolean}}

==Returns==
:;currencyInfo:{{apitype|ItemPurchaseCurrency}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| iconFileID || {{apitype|number?}} || 
|-
| currencyCount || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|}
```