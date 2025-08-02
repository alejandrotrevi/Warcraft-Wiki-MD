# API GetLFGDungeonRewardCapBarInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the weekly limits reward for a currency (e.g. Valor Point Cap).
 currencyID, dungeonID, quantity, limit, overallQuantity, overallLimit, periodPurseQuantity, periodPurseLimit, purseQuantity, purseLimit = GetLFGDungeonRewardCapBarInfo(dungeonID)

==Arguments==
:;dungeonID:{{apitype|number}}: id of the dungeon type for which information is being sought.

==Returns==
:;currencyID:{{apitype|number}} - ID for the currency
:;dungeonID:{{apitype|number}} - ID for the dungeon type
:;quantity:{{apitype|number}} - Quantity gained from basic dungeons
:;limit:{{apitype|number}} - Limit gained from basic dungeons
:;overallQuantity:{{apitype|number}} - Quantity gained from high end dungeons (Zandalari)
:;overallLimit:{{apitype|number}} - Limit gained from high end dungeons (Zandalari)
:;periodPurseQuantity:{{apitype|number}} - Quantity gained from all sources (raids)
:;periodPurseLimit:{{apitype|number}} - Limit gained from all sources (raids)
:;purseQuantity:{{apitype|number}} - Currently possessed amount
:;purseLimit:{{apitype|number}} - Limit for possessed amount
```