# API SortGuildRoster

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sorts the guild roster on a certain column.
 SortGuildRoster(sortType)

==Arguments==
:;sortType:{{apitype|string}} - The column for sorting. Chose from: {"name", "rank", "note", "online", "zone", "level",  "class"}

==Example==
 SortGuildRoster("level")
```