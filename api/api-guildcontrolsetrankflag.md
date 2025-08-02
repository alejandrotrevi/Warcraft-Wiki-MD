# API GuildControlSetRankFlag

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Sets guild rank permissions.
 GuildControlSetRankFlag(index, enabled)

==Arguments==
:;index:{{apitype|number}} - the flag index, between 1 and [[API GuildControlGetNumRanks|GuildControlGetNumRanks]]().
:;enabled:{{apitype|boolean}} - whether the flag is enabled or disabled.

==Details==
* Calling this API changes the value of the current rank flags. This changes are not saved until a call to [[API GuildControlSaveRank|GuildControlSaveRank]]() is made.
* Flag indices:
{{:Const_GUILDCONTROL_OPTION}}

==Patch changes==
* {{Patch 7.3.0|note=This function can now only be called from a secure execution path.}}
```