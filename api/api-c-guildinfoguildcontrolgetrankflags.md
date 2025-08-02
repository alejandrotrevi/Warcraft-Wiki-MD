# API C GuildInfo.GuildControlGetRankFlags

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the permission flags for a rank index.
 permissions = C_GuildInfo.GuildControlGetRankFlags(rankOrder)

==Arguments==
:;rankOrder:{{apitype|number}} - Starting at 1 (Guild Master)

==Returns==
:;permissions:{{apitype|boolean[]}} - table indices ranging from 1 to 21.
{{:Const_GUILDCONTROL_OPTION}}

==Patch changes==
* {{Patch 8.0.1|note=Added. Replaces {{api|GuildControlGetRankFlags}}.}}
```