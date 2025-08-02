# API GetArenaTeamIndexBySize

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index of an arena team for the specified team size.
 index = GetArenaTeamIndexBySize(size)

==Arguments==
:;size:{{apitype|number}} - team size (number of people), i.e. 2, 3, or 5.

==Returns==
:;index:{{apitype|number}} - arena team index for the specified team size, or nil if the player is not in a team of the specified size.

==Details==
* Arena team indices typically correspond to their creation/join order, and may be discontinuous.
* You can get information about a given team from its index using {{api|GetArenaTeam}}.

==Patch changes==
* {{Patch 5.4.0|note=Fixed arena teams removed.}}
* {{Patch 5.2.0|note=Added.}}
```