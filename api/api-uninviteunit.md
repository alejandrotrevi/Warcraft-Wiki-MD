# API UninviteUnit

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent}}
Removes a player from the group if you're the leader, or initiates a vote to kick.
 UninviteUnit(name [, reason])

==Arguments==
:;name:{{apitype|string}} - Name of the player to remove from group. When removing cross-server players, it is important to include the server name: "Ygramul-Emerald Dream".
:;reason:{{apitype|string?}} - Used when initiating a kick vote against the player.

==Details==
* If you're in a Dungeon Finder group and call UninviteUnit without providing a reason, the {{api|t=e|VOTE_KICK_REASON_NEEDED}} event will fire to notify you that a reason is required to initiate a kick vote.

==History==
* The first argument to this function was changed from "unit" to "name" in [[Patch 3.0.8]].
* The reason argument was added in [[Patch 3.3.3]]; previously, kick votes did not require a reason.
```