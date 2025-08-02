# API C TradeSkillUI.GetRecipeRequirements

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Needs summary.
 requirements = C_TradeSkillUI.GetRecipeRequirements(recipeID)

==Arguments==
:;recipeID:{{apitype|number}}

==Returns==
:;requirements:{{apitype|CraftingRecipeRequirement[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| met || {{apitype|boolean}} || 
|-
| type || {{apitype|Enum.RecipeRequirementType}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.RecipeRequirementType
! Value !! Field !! Description
|-
| 0 || SpellFocus || 
|-
| 1 || Totem || 
|-
| 2 || Area || 
|}
```