# API GetSavedInstanceInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns instance lock info.
 name, lockoutId, reset, difficultyId, locked, extended, instanceIDMostSig, isRaid, maxPlayers, difficultyName, numEncounters, encounterProgress, extendDisabled, instanceId = GetSavedInstanceInfo(index)

==Arguments==
:;index:{{apitype|number}} - index of the saved instance, from 1 to {{api|t=a|GetNumSavedInstances}}()

==Returns==
:;1. name:{{apitype|string}} - the name of the instance
:;2. lockoutId:{{apitype|number}} - the ID of the instance lockout
:;3. reset:{{apitype|number}} - the number of seconds remaining until the instance resets
:;4. difficultyId:{{apitype|number}} : [[DifficultyID]]
:;5. locked:{{apitype|boolean}} - true if the instance is currently locked, false for a historic entry
:;6. extended:{{apitype|boolean}} - shows true if the ID has been extended
:;7. instanceIDMostSig:{{apitype|number}} - unknown
:;8. isRaid:{{apitype|boolean}} - shows true if it is a raid
:;9. maxPlayers:{{apitype|number}} - shows the max players
:;10. difficultyName:{{apitype|string}} - shows a localized string i.e. 10 Player (Heroic)
:;11. numEncounters:{{apitype|number}} - number of boss encounters in this instance
:;12. encounterProgress:{{apitype|number}} - farthest boss encounter in this instance for player
:;13. extendDisabled:{{apitype|boolean}} - returns whether this instance cannot be disabled
:;14. instanceId:{{apitype|number}} : [[InstanceID]]

==Patch changes==
* {{Patch 10.0.5|note=Added <code>instanceId</code> return value.}}
* {{Patch 4.0.1|note=Added <code>numEncounters, encounterProgress</code> return values.}}
* {{Patch 3.2.0|note=Added <code>locked, extended, instanceIDMostSig, isRaid, maxPlayers, difficultyName</code> return values.}}
* {{Patch 3.0.2|note=Added <code>difficultyId</code> return value.}}
* {{Patch 1.11.0|note=Added.}}

==See also==
* {{api|GetInstanceLockTimeRemaining}} - Older, more limited version of this function
* {{api|GetNumSavedInstances}} - Counts number of instances this function applies to
* {{api|GetSavedInstanceEncounterInfo}} - A more specific function; this lets you check up on the individual encounters within a given saved instance
* {{api|GetSavedWorldBossInfo}} - A similar function to this, except for the player's saved world boss lockout data
* {{api|GetLFGDungeonInfo}} - A moderately similar function to this function, except it works off of dungeon IDs instead of saved instance indexes. It can also return Raid Finder instance info, unlike this function.
* {{api|GetRFDungeonInfo}} - Nearly identical to {{api|GetLFGDungeonInfo}}, except it uses Raid Finder indexes instead of dungeon IDs
```