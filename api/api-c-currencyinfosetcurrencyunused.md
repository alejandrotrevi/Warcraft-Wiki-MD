# API C CurrencyInfo.SetCurrencyUnused

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CurrencyInfo|system=CurrencySystem}}
Marks a currency as unused in the currency tab.
 C_CurrencyInfo.SetCurrencyUnused(index, unused)

==Arguments==
:;index:{{apitype|number}}
:;unused:{{apitype|boolean}}

==Details==
* When a currency is marked as unused, it is is placed under the "Unused" header in the currency list; this is always the last header in the list. This alters the currency's index in the currency list.
* The <code>isTypeUnused</code> return value of {{api|t=a|C_CurrencyInfo.GetCurrencyListInfo}}() can be used to get the current state.

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_CurrencyInfo.SetCurrencyUnused()</code>}}
* {{Patch 3.1.0|note=Added as <code>SetCurrencyUnused()</code>}}
```