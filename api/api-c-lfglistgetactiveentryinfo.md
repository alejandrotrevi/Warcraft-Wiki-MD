# API C LFGList.GetActiveEntryInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LFGList|system=LFGList}}
Returns information about your currently listed group.
 entryData = C_LFGList.GetActiveEntryInfo()

==Returns==
:;entryData:{{apitype|LfgEntryData}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| <s><font color="red">{{apiname|activityID}}</font></s> || {{apitype|number}} || The activityID of the group. Use [[API_C_LFGList.GetActivityInfo|C_LFGList.GetActivityInfo]](activityID) to get more information about the activity.
|-
| {{apiname|activityIDs}} || {{apitype|number[]}} || List of activity IDs for the listed group.
|-
| {{apiname|requiredItemLevel}} || {{apitype|number}} || [[Item level]] requirement for applications. Returns 0 if no requirement is set.
|-
| {{apiname|requiredHonorLevel}} || {{apitype|number}} || 
|-
| {{apiname|name}} || {{apitype|kstringLfgListApplicant}} || [[UI_escape_sequences#Protected_strings|Protected string]]
|-
| {{apiname|comment}} || {{apitype|kstringLfgListApplicant}} || Protected string
|-
| {{apiname|voiceChat}} || {{apitype|kstringLfgListApplicant}} || [[Voice_over_Internet_Protocol#World_of_Warcraft_Voice_Chat|Voice chat]] specified by group creator. Returns an empty string if no voice chat is specified.
|-
| {{apiname|duration}} || {{apitype|time_t}} || Expiration time of the group in seconds. Currently starts at 1800 seconds (30 minutes).<br>If no player joins the group within this time the group is delisted for inactivity.
|-
| {{apiname|autoAccept}} || {{apitype|boolean}} || If new applicants are automatically invited.
|-
| {{apiname|privateGroup}} || {{apitype|boolean}} || 
|-
| {{apiname|questID}} || {{apitype|number?}} || 
|-
| {{apiname|requiredDungeonScore}} || {{apitype|number?}} || 
|-
| {{apiname|requiredPvpRating}} || {{apitype|number?}} || 
|-
| {{apiname|playstyle}} || {{apitype|Enum.LFGEntryPlaystyle?}} || 
|-
| {{apiname|isCrossFactionListing}} || {{apitype|boolean}} || <font color="green">9.2.5</font>
|-
| {{apiname|newPlayerFriendly}} || {{apitype|boolean}} || <font color="green">11.0.7</font>
|}

{{:Enum.LFGEntryPlaystyle}}

==Patch changes==
* {{Patch 10.2.7|note=Changed <code>activityID</code> return value to <code>activityIDs</code>.}}
* {{Patch 9.2.5|note=Added <code>isCrossFactionListing</code> field.}}
* {{Patch 9.1.5|note=Added <code>requiredDungeonScore, requiredPvpRating, playstyle</code> fields.}}
* {{Patch 8.1.0|note=Returns structured data.}}
* {{Patch 6.0.2|note=Added.}}
```