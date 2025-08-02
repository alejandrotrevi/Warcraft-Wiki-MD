# API GuildControlSaveRank

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Saves the current rank name.
 GuildControlSaveRank(name)

==Arguments==
:;name:{{apitype|string}} - the name of this rank

==Details==
* Saves the current flags, set using [[API GuildControlSetRankFlag|GuildControlSetRankFlag]]() to the current rank.
* Entering a name different to that of the rank set with [[API GuildControlSetRank|GuildControlSetRank]]() will change the name of the current rank to the entered name.
```