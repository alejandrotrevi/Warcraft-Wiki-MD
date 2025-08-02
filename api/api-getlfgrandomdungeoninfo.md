# API GetLFGRandomDungeonInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a LFG random dungeon.
 id, name, typeID, subtypeID, minLevel, maxLevel, recLevel, minRecLevel, maxRecLevel, expansionLevel, groupID, textureFilename, difficultyID, maxPlayers, description, isHoliday, bonusRepAmount, minPlayers, isTimeWalker, name2, minGearLevel, isScalingDungeon = GetLFGRandomDungeonInfo(index)

==Arguments==
:;index:{{apitype|number}} - index of a LFG random dungeon, from 1 to {{api|GetNumRandomDungeons}}()

==Returns==
:;1. id:{{apitype|number}}
:;2. name:{{apitype|string}} - The name of the dungeon/event
:;3. typeID:{{apitype|number}} - 1=TYPEID_DUNGEON or LFR, 2=raid instance, 4=outdoor area, 6=TYPEID_RANDOM_DUNGEON
:;4. subtypeID:{{apitype|number}} - 0=Unknown, 1=LFG_SUBTYPEID_DUNGEON, 2=LFG_SUBTYPEID_HEROIC, 3=LFG_SUBTYPEID_RAID, 4=LFG_SUBTYPEID_SCENARIO, 5=LFG_SUBTYPEID_FLEXRAID
:;5. minLevel:{{apitype|number}} - Earliest level permitted to walk into the instance portal
:;6. maxLevel:{{apitype|number}} - Highest level permitted to walk into the instance portal
:;7. recLevel:{{apitype|number}} - Recommended level to queue for this dungeon
:;8. minRecLevel:{{apitype|number}} - Earliest level to queue for this dungeon
:;9. maxRecLevel:{{apitype|number}} - Highest level to queue for this dungeon
:;10. expansionLevel:{{apitype|number}} - Refers to {{api|GetAccountExpansionLevel()}} values
:;11. groupID:{{apitype|number}} - Unknown
:;12. textureFilename:{{apitype|string}} - For example "Interface\LFDFRAME\LFGIcon-%s.blp" where %s is the textureFilename value
:;13. difficultyID:{{apitype|number}} : [[DifficultyID]]
:;14. maxPlayers:{{apitype|number}} - Maximum players allowed
:;15. description:{{apitype|string}} - Usually empty for most dungeons but events contain descriptions of the event, like Love is in the Air daily or Brewfest, e.g. (string)
:;16. isHoliday:{{apitype|boolean}} - If true then this is a holiday event
:;17. bonusRepAmount:{{apitype|number}} - Unknown
:;18. minPlayers:{{apitype|number}} - Minimum number of players (before the group disbands?); usually nil
:;19. isTimeWalker:{{apitype|boolean}} - If true then it's Timewalking Dungeon
:;20. name2:{{apitype|string}} - Currently unknown.  ''Note: seems to show the alternative name used by the Instance Lockout interface, as returned by {{api|GetSavedInstanceInfo()}}.''
:;21. minGearLevel:{{apitype|number}} - The minimum average [[item level]] to queue for this dungeon; may be 0 if item level is ignored.
:;22. isScalingDungeon:{{apitype|boolean}}

==See also==
* {{api|GetSavedInstanceInfo}} - A similar function to this, except for the player's saved dungeon/raid lockout data (does not include Raid Finder)
* {{api|GetSavedWorldBossInfo}} - A similar function to this, except for the player's saved world boss lockout data
* {{api|GetRFDungeonInfo}} - Almost completely identical; this function uses Raid Finder indexes
* {{api|GetLFGDungeonInfo}} - A more specific function; this lets you check up on specific LFG Dungeons
* {{api|GetLFGDungeonEncounterInfo}} - This lets you check up on the individual encounters within a given LFG Dungeon
```