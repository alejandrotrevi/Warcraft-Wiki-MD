# API C TradeSkillUI.IsTradeSkillReady

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Checks if the Trade Skill UI is open for a profession.
 isReady = C_TradeSkillUI.IsTradeSkillReady()

==Returns==
:;isReady:{{apitype|boolean}} - true if the Trade Skill UI is open  and loaded for a profession, false otherwise.

==Details==
* The event TRADE_SKILL_UPDATE fires after UI loads all the trade skills; This can be used if isReady returns false

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|t=e|TRADE_SKILL_UPDATE}}
```