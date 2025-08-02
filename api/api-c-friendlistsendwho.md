# API C FriendList.SendWho

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_FriendList|system=FriendList}} {{restrictedapi|hwevent}}
Requests a list of other online players.
 C_FriendList.SendWho(filter, origin)

==Arguments==
:;filter:{{apitype|string}} - The criteria for which you want to perform a Who query. This can be anything for which you could normally search in a Who query:
:* Any string, which will be matched against players' names, guild names, zones and levels.
::* [[Name]] (n-"<char_name>")
::* [[Zone]] (z-"<zone_name>")
::* [[Race]] (r-"<race_name>")
::* [[Class]] (c-"<class_name>")
::* [[Guild]] (g-"<guild_name>")
::* [[Level]] ranges: (<lower_limit>-<higher_limit>)
:: These can be combined, but no more than one of each type can be searched for at once. Note that the quotation marks around the zone, race, and class must be present. Double quotation marks are required, as single quotation marks won't work.
:;origin:{{apitype|Enum.SocialWhoOrigin}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || Unknown || 
|-
| 1 || Social || 
|-
| 2 || Chat || 
|-
| 3 || Item || 
|}</onlyinclude>

==Details==
* Fires {{api|t=e|WHO_LIST_UPDATE}} when the requested query has been processed. Note that there is a server-side cooldown; queries are not guaranteed to generate a response.

==Example==
Searches for players in the level 20 to 40 range.
 C_FriendList.SendWho("20-40")

Searches for Night Elf Rogues in Teldrassil, of levels 10-15, with the string "bob" in their (guild) names.
 C_FriendList.SendWho('bob z-"Teldrassil" r-"Night Elf" c-"Rogue" 10-15')

==Patch changes==
* {{Patch 10.2.0|note=Added <code>origin</code> argument.}}
* {{Patch 8.2.5|note=(+ Patch 1.13.2) Requires a hardware event as a measure against gold spam channel invites and other unintended uses for automatically querying player names.}}
* {{Patch 8.1.0|note=Moved to <code>C_FriendList.SendWho()</code>}}
* {{Patch 1.0.0|note=Added as <code>SendWho()</code>}}

==See also==
* {{api|C_FriendList.GetWhoInfo}}()
* {{api|C_FriendList.SetWhoToUi}}()
```