# API GetNumFilteredAchievements

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of achievements after filtering.
 numFiltered = GetNumFilteredAchievements()

==Returns==
:;numFiltered:{{apitype|number}} - The number of achievements that match the search string.

==Example==
The following snippet lists the names of all achievements containing the word 'flame':

 SetAchievementSearchString("flame");
 local numFiltered = GetNumFilteredAchievements();
 
 for idx = 1, numFiltered do
   local achievementID = GetFilteredAchievementID(idx);
   local _, achievementName = GetAchievementInfo(achievementID);
   print(achievementName);
 end

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|GetAchievementInfo}}
* {{api|GetFilteredAchievementID}}
* {{api|SetAchievementSearchString}}
```