# API EJ GetLootInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns loot info for an encounter or instance.
 itemID, encounterID, name, icon, slot, armorType, link = EJ_GetLootInfo(lootID)
                                                        = EJ_GetLootInfoByIndex(index [, encounterIndex])

==Arguments (EJ_GetLootInfo)==
;lootID : number

==Arguments (EJ_GetLootInfoByIndex)==
;index : number - ranging from 1 to {{api|EJ_GetNumLoot}}.
;encounterIndex : number (optional) - index of any multiple bosses that drop the same loot, ranging from 1 to {{api|EJ_GetNumEncountersForLootByIndex}}. This makes it possible for the FrameXML to show two boss names for a loot item. [https://www.townlong-yak.com/framexml/8.1.5/Blizzard_EncounterJournal/Blizzard_EncounterJournal.lua#1719]

==Returns==
;itemID : number
;encounterID : number
;name : string - item name, including quality [[UI_escape_sequences#Coloring|color escape sequence]].
;icon : number - [[FileID]]
;slot : string - [[ItemEquipLoc|INVTYPE]], e.g. "Two-Hand" or "Shoulder".
;armorType : string - e.g. "Cloth" or "Mail". The string will be colored red if the item cannot be equipped.
;link : string - [[ItemLink]]

==Triggers events==
* If loot information is not immediately available, {{api|t=e|EJ_LOOT_DATA_RECIEVED}} will fire when it is.

==Patch changes==
* {{Patch 4.2.0|note=Added.}}
```