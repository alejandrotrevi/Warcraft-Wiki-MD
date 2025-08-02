# API GetRFDungeonInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info about a Raid Finder dungeon by index. Limited by player level and other factors, so only Raid Finder dungeons listed in the LFG tool can be looked up.
 id, name, typeID, subtypeID, minLevel, maxLevel, recLevel, minRecLevel, maxRecLevel, expansionLevel, groupID, textureFilename, difficulty, maxPlayers, description, isHoliday, bonusRepAmount, minPlayers, isTimeWalking, name2, minGearLevel, isScaling, lfgMapID = GetRFDungeonInfo(index)

==Arguments==
:;index:{{apitype|number}} - index of a Raid Finder dungeon, from 1 to {{api|GetNumRFDungeons}}()

==Returns==
:;1. id:{{apitype|number}} - Dungeon ID
:;2. name:{{apitype|string}} - The name of the dungeon/event
:;3. typeID:{{apitype|number}} - 1=TYPEID_DUNGEON or LFR, 2=raid instance, 4=outdoor area, 6=TYPEID_RANDOM_DUNGEON
:;4. subtypeID:{{apitype|number}} - 0=Unknown, 1=LFG_SUBTYPEID_DUNGEON, 2=LFG_SUBTYPEID_HEROIC, 3=LFG_SUBTYPEID_RAID, 4=LFG_SUBTYPEID_SCENARIO, 5=LFG_SUBTYPEID_FLEXRAID
:;5. minLevel:{{apitype|number}} - Earliest level you can enter this dungeon (using the portal, not LFD)
:;6. maxLevel:{{apitype|number}} - Highest level you can enter this dungeon (using the portal, not LFD)
:;7. recLevel:{{apitype|number}} - Recommended level to queue up for this dungeon
:;8. minRecLevel:{{apitype|number}} - Earliest level you can queue up for the dungeon
:;9. maxRecLevel:{{apitype|number}} - Highest level you can queue up for the dungeon
:;10. expansionLevel:{{apitype|number}} - Referring to GetAccountExpansionLevel() values
:;11. groupID:{{apitype|number}} - Unknown
:;12. textureFilename:{{apitype|string}} - For example "Interface\LFDFRAME\LFGIcon-%s.blp" where %s is the textureFilename value
:;13. difficulty:{{apitype|number}} - 0 for Normal and 1 for Heroic
:;14. maxPlayers:{{apitype|number}} - Maximum players allowed
:;15. description:{{apitype|string}} - Usually empty for most dungeons but events contain descriptions of the event, like Love is in the Air daily or Brewfest, e.g. (string)
:;16. isHoliday:{{apitype|boolean}} - If true then this is a holiday event
:;17. bonusRepAmount:{{apitype|number}} - Unknown
:;18. minPlayers:{{apitype|number}} - Minimum number of players (before the group disbands?); usually nil
:;19. isTimeWalking:{{apitype|boolean}} - If true then it's Timewalking Dungeon
:;20. name2:{{apitype|string}} - Returns the name of the raid
:;21. minGearLevel:{{apitype|number}} - The minimum average [[item level]] to queue for this dungeon; may be 0 if item level is ignored.
:;22. isScaling:{{apitype|boolean}}
:;23. lfgMapID:{{apitype|number}} : [[InstanceID]]

==Example==
 /dump GetRFDungeonInfo(1)
 => 417, "Fall of Deathwing", 1, 3, 85, 85, 85, 85, 85, 3, 0, "FALLOFDEATHWING", 1, 25, "Deathwing must be destroyed, or all is lost.", false, 0, nil, false, "Dragon Soul", 0, false, 967

 /dump GetRFDungeonInfo(2)
 => 416, "The Siege of Wyrmrest Temple", 1, 3, 85, 85, 85, 85, 85, 3, 0, "SIEGEOFWYRMRESTTEMPLE", 1, 25, "Deathwing seeks to destroy Wyrmrest Temple and end the lives of the Dragon Aspects and Thrall.", false, 0, nil, false, "Dragon Soul", 0, false, 967

==See also==
* {{api|GetNumRFDungeons}} - Counts of the number of Raid Finder dungeons the player can query with this function
* {{api|GetSavedInstanceInfo}} - A similar function to this, except for the player's saved dungeon/raid lockout data (does not include Raid Finder)
* {{api|GetSavedWorldBossInfo}} - A similar function to this, except for the player's saved world boss lockout data
* {{api|GetLFGDungeonInfo}} - Almost completely identical; this function uses dungeon IDs instead of Raid Finder indexes
* {{api|GetLFGDungeonEncounterInfo}} - A more specific function; this lets you check up on the individual encounters within a given LFG Dungeon

==Patch changes==
* {{Patch 5.4.0|note=Now returns subtypeID, bonusRepAmount and minPlayers.}}
* {{Patch 4.3.0|note=Added.}}
```