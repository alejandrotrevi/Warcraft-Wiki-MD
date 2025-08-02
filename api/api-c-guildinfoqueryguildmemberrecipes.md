# API C GuildInfo.QueryGuildMemberRecipes

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Shows the guild member recipes for a profession.
 C_GuildInfo.QueryGuildMemberRecipes(guildMemberGUID, skillLineID)

==Arguments==
:;guildMemberGUID:{{apitype|string}}
:;[[TradeSkillLineID|skillLineID]]:{{apitype|number}} - Tradeskill ID

==Fires events==
* {{api|t=e|TRADE_SKILL_SHOW}} - shows the tradeskill window for the guild member.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}

==See also==
* {{api|GetGuildMemberRecipes}}()
```