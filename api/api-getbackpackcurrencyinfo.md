# API GetBackpackCurrencyInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a tracked currency in the backpack.
 name, count, icon, currencyID = GetBackpackCurrencyInfo(index)

==Arguments==
:;index:{{apitype|number}} - Index, ascending from 1 to {{api|GetNumWatchedTokens}}().

==Returns==
:;name:{{apitype|string}} - Localized currency name.
:;count:{{apitype|number}} - Amount currently possessed by the player.
:;icon:{{apitype|number}} : [[FileID]]
:;currencyID:{{apitype|number}} : [[CurrencyID]]

==Patch changes==
* {{Patch 4.0.1|note= the extraCurrencyType (Number - 0 for item-based currencies, 1 for arena points, 2 for honor points) is no longer provided.}}
* {{Patch 3.2.0|note=Up to 3 currencies may be tracked as part of the backpack display. The function does not raise errors on out of range indices.}}
```