# API GetGuildInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns guild info for a player unit.
 guildName, guildRankName, guildRankIndex, realm = GetGuildInfo(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit whose guild information you wish to query.

==Returns==
:;guildName:{{apitype|string}} - The name of the guild the unit is in (or nil?).
:;guildRankName:{{apitype|string}} - unit's rank in unit's guild.
:;guildRankIndex:{{apitype|number}} - unit's rank (index). - zero based index (0 is Guild Master, 1 and above are lower ranks)
:;realm:{{apitype|string?}} - The name of the realm the guild is in, or nil if the guild's realm is the same as your current one

==Details==
*This function only works in close proximity to the unit you are trying to get info from.  It is the same distance that the character portrait loads if you are in party with them.  It will abandon the data shortly after you leave the area, even if the portrait is remembered.
*If using with [[UnitId]] "player" on loading it happens that this value is nil even if the player is in a guild. Here's a little function which checks in the {{api|t=e|GUILD_ROSTER_UPDATE}} and {{api|t=e|PLAYER_GUILD_UPDATE}} events, if guild name is available. As long as it is not, no actions are fired by my guild event handling.

 local function IsPlayerInGuild()
     return [[API_IsInGuild|IsInGuild]]() and GetGuildInfo("player")
 end
```