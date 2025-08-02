# API C PetBattles.GetPVPMatchmakingInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns status information about the current PvP pet battle matchmaking queue.
 queueState, estimatedTime, queuedTime = C_PetBattles.GetPVPMatchmakingInfo()

==Returns==
:;queueState:{{apitype|string}} - Either "proposal", "queued", "suspended", or nil.
:;estimatedTime:{{apitype|number}} - The current estimated wait time in seconds, rounded to the nearest second.
:;queuedTime:{{apitype|number}} - The time that the queue started at, in the same format as {{api|GetTime}}().

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetBattles.AcceptQueuedPVPMatch}} - if you wanted to accept an existing match offer
* {{api|C_PetBattles.DeclineQueuedPVPMatch}} - if you wanted to decline an existing match offer
* {{api|C_PetBattles.StartPVPMatchmaking}} - if you wanted to join the matchmaking queue
* {{api|C_PetBattles.StopPVPMatchmaking}} - if you wanted to leave the matchmaking queue
* [[World_of_Warcraft_API#Pet_Battle_Functions | Pet Battle Functions]]
```