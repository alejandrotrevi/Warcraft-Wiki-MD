# API GetInstanceInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the map instance the character is currently in.
 name, instanceType, difficultyID, difficultyName, maxPlayers, dynamicDifficulty, isDynamic, instanceID, instanceGroupSize, LfgDungeonID = GetInstanceInfo()

==Returns==
:;1. name:{{apitype|string}} - The localized name of the instance—otherwise, the continent name (e.g., Eastern Kingdoms, Kalimdor, Outland, Northrend, Pandaria).
:;2. instanceType:{{apitype|string}} - "none" if the player is not in an instance, "scenario" for scenarios, "party" for dungeons, "raid" for raids, "arena" for arenas, and "pvp" for battlegrounds.  Many of the following return values will be nil or otherwise useless in the case of "none".
:;3. difficultyID:{{apitype|number}} - The [[DifficultyID]] of the instance. Will return 0 while not in an instance.
:;4. difficultyName:{{apitype|string}} - The localized name for the instance's difficulty ("10 Player", "25 Player (Heroic)", etc.).
:;5. maxPlayers:{{apitype|number}} - Maximum number of players permitted within the instance at the same time.
:;6. dynamicDifficulty:{{apitype|number}} - The difficulty of dynamic enabled instances. This no longer appears to be used.
:;7. isDynamic:{{apitype|boolean}} - If the instance difficulty can be changed while zoned in. This is true for most raids after and including Icecrown Citadel.
:;8. instanceID:{{apitype|number}} - The [[InstanceID]] for the instance or continent.
:;9. instanceGroupSize:{{apitype|number}} - The number of players within your instance group.
:;10. LfgDungeonID:{{apitype|number}} - The [[LfgDungeonID]] for the current instance group, nil if not in a dungeon finder group.

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|C_Map.GetBestMapForUnit}} }}
|}

==Patch changes==
* {{Patch 8.0.1|note=Now returns a LfgDungeonID, in addition to the previous returns. (Unsure when this was added, guessing 8.0.1 but could have been way earlier.)}}
* {{Patch 5.4.0|note=Now returns an instanceGroupSize. Also added a new possible difficultyID (14) for Flexible Raids.}}
* {{Patch 5.0.4|note=
:* Now returns a mapID, allowing addons to identify the current instance/continent without relying on localized names.
:* dynamicDifficulty now always returns 0, while difficultyID is updated to reflect the selected dynamic difficulty (previously, dynamicDifficulty reflected the normal/heroic switch and difficultyID the 10/25 player switch for dynamic instances).}}
* {{Patch 3.3.0|note=Additional return values were added.}}
* {{Patch 3.2.0|note=Added.}}
```