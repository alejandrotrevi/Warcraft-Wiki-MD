# API C PlayerInfo.GetPlayerMythicPlusRatingSummary

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PlayerInfo|system=PlayerInfo}}
Returns the players mythic+ rating summary which includes the runs they've completed as well as their current season m+ rating
 ratingSummary = C_PlayerInfo.GetPlayerMythicPlusRatingSummary(playerToken)

==Arguments==
:;playerToken:{{apitype|string}} : [[UnitId]] - The unit does not need to be in your group.

==Returns==
:;ratingSummary:{{apitype|MythicPlusRatingSummary}} - The current season rating and well as a list of completed mythic plus runs.
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| currentSeasonScore || {{apitype|number}} || 
|-
| runs || {{apitype|MythicPlusRatingMapSummary[]}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ MythicPlusRatingMapSummary
! Field !! Type !! Description
|-
| challengeModeID || {{apitype|number}} || 
|-
| mapScore || {{apitype|number}} || 
|-
| bestRunLevel || {{apitype|number}} || 
|-
| bestRunDurationMS || {{apitype|number}} || 
|-
| finishedSuccess || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```