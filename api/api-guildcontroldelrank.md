# API GuildControlDelRank

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Deletes a guild rank.
 GuildControlDelRank(index)

==Arguments==
:;index:{{apitype|number}} - index between 1 and {{api|GuildControlGetNumRanks}}

==Details==
* The index rank must be unused - no guildmembers may currently have that rank or any lower rank (having a higher index value).
** If the rank cannot be deleted, a message written be sent to the default chat window.
```