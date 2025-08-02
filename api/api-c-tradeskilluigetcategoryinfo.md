# API C TradeSkillUI.GetCategoryInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information for a tradeskill category.

 categoryInfo = C_TradeSkillUI.GetCategoryInfo(categoryID[, returnTable])

==Arguments==
:;categoryID:{{apitype|number}} - The ID of the tradeskill category to get information for.
:;returnTable:{{apitype|table}} - Optional. The table to return the information in.

==Returns==
:;categoryInfo:{{apitype|table}} - A table containing information for the category:
::{|class="darktable zebra sortable"
|-
! Field !! Type !! Description
|-
|-
|name||String||Name of the category
|-
|enabled||Boolean||Is the category enabled
|-
|categoryID||Number||ID of the category
|-
|parentCategoryID||Number||ID of the category above this one
|-
|type||String||How should this category be displayed in the recipe list
|-
|hasProgressBar||Boolean||Should a progress bar be displayed for this category
|-
|numIndents||Number||How deeply to indent this category in the recipe list
|-
|skillLineStartingRank||Number||At what level does this category start learning ranks
|-
|skillLineMaxLevel||Number||At what level does this category stop learning ranks
|-
|skillLineCurrentLevel||Number||Current level of category skill
|}

==Details==
* Using the optional 'returnTable' argument improves performance by not creating a new table for each call to the function. This is particularly useful when iterating over all the recipes for a trade skill.
* type has been seen as either "header", which is used for top-level expansion recipe categories, or "subheader", which is used for what in the old system were specializations (such as "Way of the Grill")

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|C_TradeSkillUI.GetRecipeInfo}}
* {{api|C_TradeSkillUI.GetTradeSkillLine}}
```