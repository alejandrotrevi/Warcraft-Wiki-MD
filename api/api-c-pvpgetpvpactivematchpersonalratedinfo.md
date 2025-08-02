# API C PvP.GetPVPActiveMatchPersonalRatedInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PvP|system=PvpInfo}}
Needs summary.
 info = C_PvP.GetPVPActiveMatchPersonalRatedInfo()

==Returns==
:;info:{{apitype|PVPPersonalRatedInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| personalRating || {{apitype|number}} || 
|-
| bestSeasonRating || {{apitype|number}} || 
|-
| bestWeeklyRating || {{apitype|number}} || 
|-
| seasonPlayed || {{apitype|number}} || 
|-
| seasonWon || {{apitype|number}} || 
|-
| weeklyPlayed || {{apitype|number}} || 
|-
| weeklyWon || {{apitype|number}} || 
|-
| lastWeeksBestRating || {{apitype|number}} || 
|-
| hasWonBracketToday || {{apitype|boolean}} || 
|-
| tier || {{apitype|number}} || 
|-
| ranking || {{apitype|number?}} || 
|-
| roundsSeasonPlayed || {{apitype|number}} || <font color="green">10.0.0</font>
|-
| roundsSeasonWon || {{apitype|number}} || <font color="green">10.0.0</font>
|-
| roundsWeeklyPlayed || {{apitype|number}} || <font color="green">10.0.0</font>
|-
| roundsWeeklyWon || {{apitype|number}} || <font color="green">10.0.0</font>
|}

==Patch changes==
* {{Patch 8.2.0|note=Added.}}
```