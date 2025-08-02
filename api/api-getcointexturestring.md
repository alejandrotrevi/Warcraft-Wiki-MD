# API GetCoinTextureString

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Breaks up an amount of money into gold/silver/copper with icons.
 formattedAmount = GetCoinTextureString(amount [, fontHeight])

==Arguments==
:;amount:{{apitype|number}} - the amount of money in copper (for example, the return value from [[API_GetMoney|GetMoney]])
:;fontHeight:{{apitype|number?}} - the height of the coin icon; if not specified, defaults to 14.

==Returns==
:;formattedAmount:{{apitype|string}} - a string suitable for printing or displaying.

==Example==
{{:API_GetMoney}}
```