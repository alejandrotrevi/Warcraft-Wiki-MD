# API C TradeSkillUI.OpenTradeSkill

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent}}
Opens a tradeskill window.
 success = C_TradeSkillUI.OpenTradeSkill(tradeSkillID)

==Arguments==
:;[[TradeSkillLineID|tradeSkillID]]:{{apitype|number}}

==Returns==
:;success:{{apitype|boolean}}

==Example==
Opens the cooking window.
 /run C_TradeSkillUI.OpenTradeSkill(185)

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```