# API C Container.GetContainerItemPurchaseInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Container|system=Container}}
Needs summary.
 info = C_Container.GetContainerItemPurchaseInfo(containerIndex, slotIndex, isEquipped)

==Arguments==
:;containerIndex:{{apitype|number}}
:;slotIndex:{{apitype|number}}
:;isEquipped:{{apitype|boolean}}

==Returns==
:;info:{{apitype|ItemPurchaseInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| money || {{apitype|number}} || 
|-
| itemCount || {{apitype|number}} || 
|-
| refundSeconds || {{apitype|number}} || 
|-
| currencyCount || {{apitype|number}} || 
|-
| hasEnchants || {{apitype|boolean}} || 
|}
```