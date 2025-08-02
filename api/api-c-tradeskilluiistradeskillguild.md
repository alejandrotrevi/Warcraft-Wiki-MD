# API C TradeSkillUI.IsTradeSkillGuild

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Checks if the Trade Skill UI is open for a profession in the guild.
 isGuild = C_TradeSkillUI.IsTradeSkillGuild()

==Returns==
:;isGuild:{{apitype|boolean}} - true if the Trade Skill UI is open for a profession in the guild, false otherwise.

==Details==
* This function will typically only be true if 'View All' has been clicked for a profession in the 'Professions' view of the guild roster.

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|C_TradeSkillUI.IsNPCCrafting}}
* {{api|C_TradeSkillUI.IsTradeSkillLinked}}
```