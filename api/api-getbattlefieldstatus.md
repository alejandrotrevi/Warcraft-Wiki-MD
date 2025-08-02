# API GetBattlefieldStatus

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the status of the battlefield the player is either queued for or inside.
 status, mapName, teamSize, registeredMatch, suspendedQueue, queueType, gameType, role, asGroup, shortDescription, longDescription, isSoloQueue = GetBattlefieldStatus(index)

==Arguments==
:;index:{{apitype|number}} - Index of the battlefield you wish to view, in the range of 1 to [[API_GetMaxBattlefieldID|GetMaxBattlefieldID]]()

==Returns==
:;1. status:{{apitype|string}} - Battlefield status, one of:
::* queued - Waiting for a battlefield to become ready, you're in the queue
::* confirm - Ready to join a battlefield
::* active - Inside an active battlefield
::* none - Not queued for anything in this index
::* error - This should never happen
:;2. mapName:{{apitype|string}} - Localized name of the battlefield (eg. [[Warsong Gulch]] or [[Blade's Edge Arena]])
:;3. teamSize:{{apitype|number}} - Team size of the battlefields queue (2, 3 or 5 in an arena queue, or 0 in other queue types)
:;4. registeredMatch:{{apitype|boolean}} - true in a registered arena queue, or false in a skirimish or non-arena queue; use teamSize to check for arenas.
:;5. suspendedQueue:{{apitype|boolean}} - (used to determine whether the eye icon on the LFG minimap button should animate, presumed boolean or 1/nil)
:;6. queueType:{{apitype|string}} - The type of battleground, one of:
::* ARENA
::* BATTLEGROUND
::* WARGAME
:;7. gameType:{{apitype|string}} - ??? (displayed as-is to the user on the queue ready dialog, so presumed localized; can be an empty string)
:;8. role:{{apitype|string}} - The role assigned to the player (TANK, DAMAGER, HEALER) in a non-rated battleground, or nil for other queue types.
:;9. asGroup:{{apitype|boolean}}
:;10. shortDescription:{{apitype|string}}
:;11. longDescription:{{apitype|string}}
:;12. isSoloQueue:{{apitype|boolean}}

==Patch changes==
* {{Patch 10.0.7|note=Added <code>isSoloQueue</code>.}}
* {{Patch 5.2.0|note=Return values changed. Removed <code>instanceID</code>, <code>lowestLevel</code> and <code>highestLevel</code>. Added <code>suspendedQueue</code>, <code>queueType</code>, <code>gameType</code> and <code>role</code>.}}
```