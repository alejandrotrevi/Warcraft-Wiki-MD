# API GetFilteredAchievementID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the ID of a filtered achievement by index.
 achievementID = GetFilteredAchievementID(index)

==Arguments==
:;index:{{apitype|number}} - The index of the filtered achievement to return the ID of, between 1 and {{api|GetNumFilteredAchievements}}().

==Returns==
:;achievementID:{{apitype|number}} - The ID of an achievement.

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
* {{api|GetNumFilteredAchievements}}
* {{api|SetAchievementSearchString}}
```