# API GuildControlSetRank

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Selects a guild rank.
 GuildControlSetRank(rankOrder)

==Arguments==
:;rankOrder:{{apitype|number}} - index of the rank to select, between 1 and {{api|GuildControlGetNumRanks}}().

==Details==
* Calling this API sets the rank to return/edit flags for using {{api|GuildControlGetRankFlags}}() and {{api|GuildControlSetRankFlag}}().

==Patch changes==
* {{Patch 7.3.0|note=This function can now only be called from a secure execution path.}}
```