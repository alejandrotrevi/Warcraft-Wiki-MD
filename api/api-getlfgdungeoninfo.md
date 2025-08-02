# API GetLFGDungeonInfo

**Contributor:** Nathanyel

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a LFG dungeon.
 name, typeID, subtypeID, minLevel, maxLevel, recLevel, minRecLevel, maxRecLevel, expansionLevel, groupID, textureFilename, difficulty, maxPlayers, description, isHoliday, bonusRepAmount, minPlayers, isTimeWalker, name2, minGearLevel, isScalingDungeon, lfgMapID = GetLFGDungeonInfo(dungeonID)

==Arguments==
:;dungeonID:{{apitype|number}} : [[LfgDungeonID]]

==Returns==
:;1. name:{{apitype|string}} - The name of the dungeon/event
:;2. typeID:{{apitype|number}} - 1=TYPEID_DUNGEON or LFR, 2=raid instance, 4=outdoor area, 6=TYPEID_RANDOM_DUNGEON
:;3. subtypeID:{{apitype|number}} - 0=Unknown, 1=LFG_SUBTYPEID_DUNGEON, 2=LFG_SUBTYPEID_HEROIC, 3=LFG_SUBTYPEID_RAID, 4=LFG_SUBTYPEID_SCENARIO, 5=LFG_SUBTYPEID_FLEXRAID
:;4. minLevel:{{apitype|number}} - Earliest level permitted to walk into the instance portal
:;5. maxLevel:{{apitype|number}} - Highest level permitted to walk into the instance portal
:;6. recLevel:{{apitype|number}} - Recommended level to queue for this dungeon
:;7. minRecLevel:{{apitype|number}} - Earliest level to queue for this dungeon
:;8. maxRecLevel:{{apitype|number}} - Highest level to queue for this dungeon
:;9. expansionLevel:{{apitype|number}} - Refers to {{api|GetAccountExpansionLevel()}} values
:;10. groupID:{{apitype|number}} - Unknown
:;11. textureFilename:{{apitype|string}} - For example "Interface\LFDFRAME\LFGIcon-%s.blp" where %s is the textureFilename value
:;12. difficulty:{{apitype|number}} : [[DifficultyID]]
:;13. maxPlayers:{{apitype|number}} - Maximum players allowed
:;14. description:{{apitype|string}} - Usually empty for most dungeons but events contain descriptions of the event, like Love is in the Air daily or Brewfest, e.g. (string)
:;15. isHoliday:{{apitype|boolean}} - If true then this is a holiday event
:;16. bonusRepAmount:{{apitype|number}} - Unknown
:;17. minPlayers:{{apitype|number}} - Minimum number of players (before the group disbands?); usually nil
:;18. isTimeWalker:{{apitype|boolean}} - If true then it's Timewalking Dungeon (false during [[Turbulent Timeways]] events)
:;19. name2:{{apitype|string}} - Currently unknown.  ''Note: seems to show the alternative name used by the Instance Lockout interface, as returned by {{api|GetSavedInstanceInfo()}}.''
:;20. minGearLevel:{{apitype|number}} - The minimum average [[item level]] to queue for this dungeon; may be 0 if item level is ignored.
:;21. isScalingDungeon:{{apitype|boolean}}
:;22. lfgMapID:{{apitype|number}} : [[InstanceID]]

==Patch changes==
* {{Patch 8.3.0|note=Added <code>lfgMapID</code> return.}}
* {{Patch 7.3.5|note=Added <code>isScalingDungeon</code> return.}}
* {{Patch 7.0.3|note=Added <code>isTimeWalker, name2, minGearLevel</code> returns.}}
* {{Patch 5.4.0|note=Added <code>subtypeID, bonusRepAmount and minPlayers</code> returns.}}
* {{Patch 4.3.0|note=Added. Replaces {{api|LFGGetDungeonInfoByID}}()}}

==See also==
* {{api|GetSavedInstanceInfo}} - A similar function to this, except for the player's saved dungeon/raid lockout data (does not include Raid Finder)
* {{api|GetSavedWorldBossInfo}} - A similar function to this, except for the player's saved world boss lockout data
* {{api|GetRFDungeonInfo}} - Almost completely identical; this function uses Raid Finder indexes instead of dungeon IDs
* {{api|GetLFGDungeonEncounterInfo}} - A more specific function; this lets you check up on the individual encounters within a given LFG Dungeon
```