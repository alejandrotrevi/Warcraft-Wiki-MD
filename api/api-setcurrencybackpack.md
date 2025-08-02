# API SetCurrencyBackpack

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Alters the backpack tracking state of a currency.
 SetCurrencyBackpack(id, backpack)

== Arguments ==
; id : Number - Index of the currency in the currency list to alter tracking of.
; backpack : Number - 1 to track; 0 to clear tracking.

== Notes ==
* This function affects the isWatched return value of {{api|GetCurrencyListInfo}}.
* Information about watched currencies is accessible using {{api|GetBackpackCurrencyListInfo}}.
```