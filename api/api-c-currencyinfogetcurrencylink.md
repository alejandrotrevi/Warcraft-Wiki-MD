# API C CurrencyInfo.GetCurrencyLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CurrencyInfo|system=CurrencySystem}}
Returns a currency link.
 link = C_CurrencyInfo.GetCurrencyLink(type [, amount])

==Arguments==
:;type:{{apitype|number}} : [[CurrencyID]]
:;amount:{{apitype|number?}}

==Returns==
:;link:{{apitype|string}} : [[Hyperlinks#currency|currencyLink]]

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_CurrencyInfo.GetCurrencyLink()</code>}}
* {{Patch 4.2.0|note=Added as <code>GetCurrencyLink()</code>}}
```