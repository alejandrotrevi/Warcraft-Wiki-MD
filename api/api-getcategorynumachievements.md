# API GetCategoryNumAchievements

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of achievements for a category.
 total, completed, incompleted = GetCategoryNumAchievements(categoryId [, includeAll])

==Arguments==
:;categoryId:{{apitype|number}} - Achievement category ID, as returned by {{api|GetCategoryList}}.
:;includeAll:{{apitype|boolean?}} - If true-equivalent, include all achievements, otherwise, only includes those currently visible

==Returns==
:;total:{{apitype|number}} - total number of achievements in the specified category.
:;completed:{{apitype|number}} - number of completed achievements in the specified category.
:;incompleted:{{apitype|number}} - number of incompleted achievements in the specified category.

==Example==
The snippet below prints the achievement IDs and names of all achievements in the World Events > Midsummer category:
 for i=1, (GetCategoryNumAchievements(161)) do
  local id, name = GetAchievementInfo(161, i)
  print(id, name)
 end

==See also==
* {{api|GetCategoryList}}
* {{api|GetAchievementInfo}}(categoryId, index)

==Patch changes==
* {{Patch 3.0.2|note=Added.}}
```