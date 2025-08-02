# API SetAchievementSearchString

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Starts a search for achievements containing the specified text.

 searchFinished = SetAchievementSearchString(searchText)

==Arguments==
:;searchText:{{apitype|string}} - Text to search for in the achievements.

==Returns==
:;searchFinished:{{apitype|boolean}} - true if the search is finished, false otherwise.

==Triggers events==
* {{api|t=e|ACHIEVEMENT_SEARCH_UPDATED}}, when the search has finished and the filtered results are available.

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|GetFilteredAchievementID}}
* {{api|GetNumFilteredAchievements}}
```