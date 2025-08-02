# API C MythicPlus.GetSeasonBestForMap

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MythicPlus|system=MythicPlusInfo}}
Returns your best intime and overtime runs of the season, irrespective of the run's affix, or the current week's affix.
 intimeInfo, overtimeInfo = C_MythicPlus.GetSeasonBestForMap(mapChallengeModeID)

==Arguments==
:;mapChallengeModeID:{{apitype|number}} : [https://wago.tools/db2/MapChallengeMode MapChallengeMode.ID]

==Returns==
:;intimeInfo:{{apitype|MapSeasonBestInfo?}} - your highest rating run, that was completed in time. Nil if you've not completed any run in time this season.
:;overtimeInfo:{{apitype|MapSeasonBestInfo?}} - your highest rating run, that was '''not''' completed in time. Nil if you've only ever completed runs in time this season.
{{:Struct MapSeasonBestInfo}}

==Patch changes==
* {{Patch 9.1.0|note=Added <code>dungeonScore</code> field.}}
* {{Patch 8.1.0|note=Returns structured data.}}
* {{Patch 8.0.1|note=Added.}}
```