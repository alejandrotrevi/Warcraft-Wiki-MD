# API C LFGList.GetSearchResultInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LFGList|system=LFGList}}
Needs summary.
 searchResultData = C_LFGList.GetSearchResultInfo(searchResultID)

==Arguments==
:;searchResultID:{{apitype|number}}

==Returns==
[[File:API_C_LFGList.GetSearchResultInfo.png|frame|right]]
:;searchResultData:{{apitype|LfgSearchResultData}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|searchResultID}} || {{apitype|number}} || 
|-
| {{apiname|activityIDs}} || {{apitype|number[]}} || <font color="green">11.0.7</font> - List of activity IDs for the found group.
|-
| {{apiname|leaderName}} || {{apitype|string?}} || 
|-
| {{apiname|name}} || {{apitype|kstringLfgListSearch}} || [[UI_escape_sequences#Protected_strings|Protected string]]
|-
| {{apiname|comment}} || {{apitype|kstringLfgListSearch}} || Protected string
|-
| {{apiname|voiceChat}} || {{apitype|kstringLfgListSearch}} || 
|-
| {{apiname|requiredItemLevel}} || {{apitype|number}} || 
|-
| {{apiname|requiredHonorLevel}} || {{apitype|number}} || 
|-
| {{apiname|hasSelf}} || {{apitype|boolean}} || <font color="green">10.0.0</font>
|-
| {{apiname|numMembers}} || {{apitype|number}} || 
|-
| {{apiname|numBNetFriends}} || {{apitype|number}} || 
|-
| {{apiname|numCharFriends}} || {{apitype|number}} || 
|-
| {{apiname|numGuildMates}} || {{apitype|number}} || 
|-
| {{apiname|isDelisted}} || {{apitype|boolean}} || 
|-
| {{apiname|autoAccept}} || {{apitype|boolean}} || 
|-
| {{apiname|isWarMode}} || {{apitype|boolean}} || 
|-
| {{apiname|age}} || {{apitype|time_t}} || 
|-
| {{apiname|questID}} || {{apitype|number?}} || 
|-
| {{apiname|leaderOverallDungeonScore}} || {{apitype|number?}} || 
|-
| {{apiname|leaderDungeonScoreInfo}} || {{apitype|BestDungeonScoreMapInfo[]}} || 
|-
| {{apiname|leaderBestDungeonScoreInfo}} || {{apitype|BestDungeonScoreMapInfo?}} || <font color="green">10.2.7</font>
|-
| {{apiname|leaderPvpRatingInfo}} || {{apitype|PvpRatingInfo[]}} || 
|-
| {{apiname|requiredDungeonScore}} || {{apitype|number?}} || 
|-
| {{apiname|requiredPvpRating}} || {{apitype|number?}} || 
|-
| {{apiname|playstyle}} || {{apitype|Enum.LFGEntryPlaystyle?}} || 
|-
| {{apiname|crossFactionListing}} || {{apitype|boolean?}} || <font color="green">9.2.5</font>
|-
| {{apiname|leaderFactionGroup}} || {{apitype|number}} || <font color="green">9.2.5</font>
|-
| {{apiname|newPlayerFriendly}} || {{apitype|boolean?}} || <font color="green">11.0.7</font>
|-
| {{apiname|partyGUID}} || {{apitype|WOWGUID}} || <font color="green">11.0.0</font>
|}

{{:Struct BestDungeonScoreMapInfo}}

{{:Struct PvpRatingInfo}}

{{:Enum.LFGEntryPlaystyle}}

==Patch changes==
* {{Patch 11.0.7|note=Changed <code>activityID</code> field to <code>activityIDs</code>.}}
* {{Patch 9.2.5|note=Added <code>isCrossFactionListing, leaderFactionGroup</code> fields.}}
* {{Patch 9.1.5|note=Added <code>leaderPvpRatingInfo, requiredDungeonScore, requiredPvpRating, playstyle</code> fields.}}
* {{Patch 9.1.0|note=Added <code>isWarMode, leaderOverallDungeonScore, leaderDungeonScoreInfo</code> fields.}}
* {{Patch 8.1.0|note=Returns structured data.}}
* {{Patch 6.0.2|note=Added.}}
```