# API C TradeSkillUI.GetCategories

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a table of category IDs for the currently opened trade skill.
 categoryIDs = C_TradeSkillUI.GetCategories()

==Returns==
:;categoryIDs:{{apitype|number[]}}

==Example==
This lists all categories for the currently opened profession.
<syntaxhighlight lang="lua">
local categories = {C_TradeSkillUI.GetCategories()}

for _, categoryID in pairs(categories) do
	print(categoryID, C_TradeSkillUI.GetCategoryInfo(categoryID).name)
end
</syntaxhighlight>

==Patch changes==
* {{Patch 8.0.1|note=Changed to return a table (Build 26231).}}
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|C_TradeSkillUI.GetCategoryInfo}}
* {{api|C_TradeSkillUI.IsEmptySkillLineCategory}}
```