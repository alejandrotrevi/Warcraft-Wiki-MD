# API C MythicPlus.GetWeeklyBestForMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MythicPlus|system=MythicPlusInfo}}
Needs summary.
 durationSec, level, completionDate, affixIDs, members, dungeonScore = C_MythicPlus.GetWeeklyBestForMap(mapChallengeModeID)

==Arguments==
:;mapChallengeModeID:{{apitype|number}} : {{dbc|mapchallengemode|MapChallengeMode.ID}}

==Returns==
:;durationSec:{{apitype|number}}
:;level:{{apitype|number}}
:;completionDate:{{apitype|MythicPlusDate}}
{{:Struct MythicPlusDate|nocaption=1}}
:;affixIDs:{{apitype|number[]}}
:;members:{{apitype|MythicPlusMember[]}}
{{:Struct MythicPlusMember|nocaption=1}}
:;dungeonScore:{{apitype|number}}

==Patch changes==
* {{Patch 9.1.0|note=Added <code>dungeonScore</code> return.}}
* {{Patch 8.0.1|note=Added.}}
```