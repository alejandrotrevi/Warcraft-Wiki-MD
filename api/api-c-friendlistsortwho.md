# API C FriendList.SortWho

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sorts the last [[MACRO_who|/who]] reply received by the client.
 C_FriendList.SortWho(sorting)

==Arguments==
:;sorting:{{apitype|string}} - The column by which you wish to sort the who list:
:: "name" (default), "level", "class", "zone", "guild", "race"

==Triggers events==
* {{api|t=e|WHO_LIST_UPDATE}} is fired when the list is sorted

==Details==
* This function changes the mapping between {{api|C_FriendList.GetWhoInfo}} indices and result rows.
* FrameXML will show the who frame on this event, even if it was not visible before.
* Calling the same sort twice will reverse the sort.
* You may sort by guild, race, or zone even if it is not the currently selected second column on the who frame.

==Patch changes==
* {{Patch 8.1.0|note=Moved to ''C_FriendList''. The former alias {{api|SortWho}} is deprecated and will be removed in the following expansion.[https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#187]}}
```