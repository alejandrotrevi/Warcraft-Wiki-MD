# API C CurrencyInfo.GetBackpackCurrencyInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CurrencyInfo|system=CurrencySystem}}
Returns info for a tracked currency in the backpack.
 info = C_CurrencyInfo.GetBackpackCurrencyInfo(index)

==Arguments==
:;index:{{apitype|number}}

==Returns==
:;info:{{apitype|BackpackCurrencyInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| quantity || {{apitype|number}} || 
|-
| iconFileID || {{apitype|number}} || 
|-
| currencyTypesID || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_CurrencyInfo.GetBackpackCurrencyInfo()</code>}}
* {{Patch 3.1.0|note=Added as <code>name, count, icon, currencyID = GetBackpackCurrencyInfo(index)</code>}}
```