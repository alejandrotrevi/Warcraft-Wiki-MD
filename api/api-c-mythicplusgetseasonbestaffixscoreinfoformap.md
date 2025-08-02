# API C MythicPlus.GetSeasonBestAffixScoreInfoForMap

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MythicPlus|system=MythicPlusInfo}}
Gets the active players best runs by the seasonal tracked affixes as well as their overall score for the current season.
 affixScores, bestOverAllScore = C_MythicPlus.GetSeasonBestAffixScoreInfoForMap(mapChallengeModeID)

==Arguments==
:;mapChallengeModeID:{{apitype|number}} : {{dbc|mapchallengemode|MapChallengeMode.ID}}

==Returns==
:;affixScores:{{apitype|MythicPlusAffixScoreInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| score || {{apitype|number}} || 
|-
| level || {{apitype|number}} || 
|-
| durationSec || {{apitype|number}} || 
|-
| overTime || {{apitype|boolean}} || 
|}
:;bestOverAllScore:{{apitype|number}}

==Patch changes==
* {{Patch 9.1.0|note=Added.}}

==See also==
* [[Mythic Plus Score Computation]]
```