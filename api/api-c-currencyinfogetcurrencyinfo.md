# API C CurrencyInfo.GetCurrencyInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CurrencyInfo|system=CurrencySystem}}
Returns info for a currency by ID.
 info = C_CurrencyInfo.GetCurrencyInfo(type)
      = C_CurrencyInfo.GetCurrencyInfoFromLink(link)

==Arguments==
===<font color="#4ec9b0">GetCurrencyInfo</font>===
:;type:{{apitype|number}} : [[CurrencyID]]

===<font color="#4ec9b0">GetCurrencyInfoFromLink</font>===
:;link:{{apitype|string}} : [[Hyperlinks#currency|currencyLink]]

==Returns==
:;info:{{apitype|CurrencyInfo}}
{{:Struct CurrencyInfo|nocaption=1}}

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_CurrencyInfo.GetCurrencyInfo()</code> and returns structured data.}}
* {{Patch 4.0.1|note=Added as <code>name, currentAmount, texture, earnedThisWeek, weeklyMax, totalMax, isDiscovered, rarity = GetCurrencyInfo(id)</code>}}
```