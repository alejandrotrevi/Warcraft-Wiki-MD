# API C CurrencyInfo.GetCurrencyListInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CurrencyInfo|system=CurrencySystem}}
Returns info for a currency in the [[currency tab]].
 info = C_CurrencyInfo.GetCurrencyListInfo(index)

==Arguments==
:;index:{{apitype|number}}

==Returns==
:;info:{{apitype|CurrencyInfo}}
{{:Struct CurrencyInfo|nocaption=1}}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_CurrencyInfo.GetCurrencyListInfo()</code>}}
* {{Patch 3.1.0|note=Added as <code>name, isHeader, isExpanded, isUnused, isWatched, count, icon, maximum, hasWeeklyLimit, currentWeeklyAmount, unknown, itemID = GetCurrencyListInfo(index)</code>}}
```