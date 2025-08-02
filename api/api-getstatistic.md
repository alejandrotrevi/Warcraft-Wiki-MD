# API GetStatistic

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a character statistic.
 value, skip, id = GetStatistic(category [, index])

==Arguments==
:;category:{{apitype|number}} - [[AchievementID]] of a statistic or statistic category.
:;index:{{apitype|number?}} - Entry within a statistic category, if applicable.

==Returns==
:;value:{{apitype|string}} - Value of the statistic as displayed in-game.
:;skip:{{apitype|boolean}} - Prevents a statistic from being shown in the default UI.
:;id:{{apitype|string}} - Unknown.

==Details==
* Using the achievementID's of actual Achievements, as opposed to statistics, generates strange results.  More testing is needed.
* Wrapping the returned value with {{api|tonumber()}} is necessary to do comparisons using math operators.

==Example==
Here is a function that will take any statistic title (like <code>Battlegrounds played</code>) and will return the statistic ID for that statistic, so it can be used in other functions.

<pre>
function GetStatisticId(StatisticTitle)
	for _, CategoryId in pairs(GetStatisticsCategoryList()) do	
		for i = 1, GetCategoryNumAchievements(CategoryId) do
			local IDNumber, Name = GetAchievementInfo(CategoryId, i)
			if Name == StatisticTitle then
				return IDNumber
			end
		end		
	end
	return -1
end
</pre>

==Patch changes==
* {{Patch 5.4.0|note=Added multiple return values and optional argument.<ref>{{ref FrameXML|Blizzard_AchievementUI/Blizzard_AchievementUI.lua|5.4.0|17359|1957|20130909}}</ref>}}
* {{Patch 3.0.2|note=Added.}}

==References==
{{Reflist}}
```