# API C TradeSkillUI.GetRecipeOutputItemData

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TradeSkillUI|system=TradeSkillUI}}
Returns an icon, item link (if any) and item ID (if any) for the expected output of a recipe, given the supplied reagents.
 outputInfo = C_TradeSkillUI.GetRecipeOutputItemData(recipeSpellID [, reagents [, allocationItemGUID [, overrideQualityID [, recraftOrderID]]]])

==Arguments==
:;recipeSpellID:{{apitype|number}}
:;reagents:{{apitype|CraftingReagentInfo[]?}}
{{:Struct CraftingReagentInfo|nocaption=1}}
:;allocationItemGUID:{{apitype|WOWGUID?}}
:;overrideQualityID:{{apitype|number?}} - Use this to specify the quality ignoring the reagents.
:;recraftOrderID:{{apitype|BigUInteger?}}

==Returns==
:;outputInfo:{{apitype|CraftingRecipeOutputInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| icon || {{apitype|number}} || 
|-
| hyperlink || {{apitype|string?}} || 
|-
| itemID || {{apitype|number?}} || 
|}

==Patch changes==
* {{Patch 10.0.5|note=Added <code>recraftOrderID</code> argument.}}
```