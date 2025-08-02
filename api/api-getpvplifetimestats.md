# API GetPVPLifetimeStats

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the character's lifetime PvP statistics.
 lifetimeHonorableKills, lifetimeMaxPVPRank = GetPVPLifetimeStats()

==Returns==
:;lifetimeHonorableKills:{{apitype|number}} - The number of honorable kills you have made
:;lifetimeMaxPVPRank:{{apitype|Enum.PvPRanks}} - The highest rank you have achieved (Use [[API GetPVPRankInfo|GetPVPRankInfo]](highestRank) to get the name of the rank)
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || {{apiname|RankNone}} || 
|-
| 1 || {{apiname|RankPariah}} || 
|-
| 2 || {{apiname|RankOutlaw}} || 
|-
| 3 || {{apiname|RankExiled}} || 
|-
| 4 || {{apiname|RankDishonored}} || 
|-
| 5 || {{apiname|Rank_1}} || 
|-
| 6 || {{apiname|Rank_2}} || 
|-
| 7 || {{apiname|Rank_3}} || 
|-
| 8 || {{apiname|Rank_4}} || 
|-
| 9 || {{apiname|Rank_5}} || 
|-
| 10 || {{apiname|Rank_6}} || 
|-
| 11 || {{apiname|Rank_7}} || 
|-
| 12 || {{apiname|Rank_8}} || 
|-
| 13 || {{apiname|Rank_9}} || 
|-
| 14 || {{apiname|Rank_10}} || 
|-
| 15 || {{apiname|Rank_11}} || 
|-
| 16 || {{apiname|Rank_12}} || 
|-
| 17 || {{apiname|Rank_13}} || 
|-
| 18 || {{apiname|Rank_14}} || 
|}

==Example==
Prints the player's PVP rank name to the default chat frame.
 local _, _, highestRank = GetPVPLifetimeStats()
 local pvpRank = GetPVPRankInfo(highestRank)
 print(pvpRank)

==Patch changes==
* Removed <code>dishonorableKills</code> return value in an unknown patch.
```