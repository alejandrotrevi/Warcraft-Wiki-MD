# API C PetBattles.CanAcceptQueuedPVPMatch

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the player can currently accept the queued PvP pet battle match.
 canAccept = C_PetBattles.CanAcceptQueuedPVPMatch()

==Returns==
:;canAccept:{{apitype|boolean}} - true if the player can currently accept the queued PvP pet battle match invitation, false otherwise.

==Details==
* Combat (and potentially other conditions) prevent the player from accepting a queued PvP pet battle.
* This function can return <code>true</code> even if the player does not have an active invitation to a PvP pet battle.

==Patch changes==
* {{Patch 5.3.0|note=Added.}}

==See also==
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```