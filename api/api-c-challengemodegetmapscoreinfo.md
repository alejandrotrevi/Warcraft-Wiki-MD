# API C ChallengeMode.GetMapScoreInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ChallengeMode|system=ChallengeModeInfo}}
Gets the player's best score information for the current weekly affix, for all maps active in the current season
 displayScores = C_ChallengeMode.GetMapScoreInfo()

==Returns==
:;displayScores:{{apitype|MythicPlusRatingLinkInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| mapChallengeModeID || {{apitype|number}} || 
|-
| level || {{apitype|number}} || the completed keystone level (defaults to 0)
|-
| completedInTime || {{apitype|number}} || 1 for in time, 0 for out of time (defaults to 0)
|-
| dungeonScore || {{apitype|number}} || the score earned for the current affix (defaults to 0)
|-
| name || {{apitype|string}} || appears to always be empty
|}

==Patch changes==
* {{Patch 9.1.5|note=Added.}}

==See also==
* [[Mythic Plus Score Computation]]
```