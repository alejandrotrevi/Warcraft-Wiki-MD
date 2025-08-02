# API C TradeSkillUI.GetRecipeRepeatCount

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.0.0}}
Returns the number of times the current item is being crafted.
 local repeatCount = C_TradeSkillUI.GetRecipeRepeatCount()

==Returns==
:;repeatCount:{{apitype|number}} - The number of times the current tradeskill item is being crafted.

==Details==
: The repeat count is initially set by the optional repeat parameter of [[API DoTradeSkill|DoTradeSkill]].

==Patch changes==
* {{Patch 7.0.3|note=Moved from {{api|GetTradeskillRepeatCount}} to {{api|C_TradeSkillUI.GetRecipeRepeatCount}}.}}
```