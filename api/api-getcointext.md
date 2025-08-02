# API GetCoinText

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Breaks up an amount of money into gold/silver/copper.
 formattedAmount = GetCoinText(amount [, separator])

==Arguments==
:;amount:{{apitype|number}} - the amount of money in copper (for example, the return value from [[API_GetMoney|GetMoney]])
:;separator:{{apitype|string?}} - a string to insert between the formatted amounts of currency, if there is more than one type

==Returns==
:;formattedAmount:{{apitype|string}} - a (presumably localized) string suitable for printing or displaying

==Example==
{{:API GetMoney}}
```