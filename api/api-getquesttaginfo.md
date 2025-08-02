# API GetQuestTagInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieves tag information about the quest.
 tagID, tagName, worldQuestType, rarity, isElite, tradeskillLineIndex, displayTimeLeft = GetQuestTagInfo(questID)

==Arguments==
:;questID:{{apitype|number}} - The ID of the quest to retrieve the tag info for.

==Returns==
:;tagID:{{apitype|number}} - the tagID, nil if quest is not tagged
:;tagName:{{apitype|string}} - human readable representation of the tagID, nil if quest is not tagged
:;worldQuestType:{{apitype|number}} - type of world quest, or nil if not world quest
:;rarity:{{apitype|number}} - the rarity of the quest (used for world quests)
:;isElite:{{apitype|boolean}} - is this an elite quest?  (used for world quests)
:;tradeskillLineIndex:tradeskillID if this is a profession quest  (used to determine which profession icon to display for world quests)
:;displayTimeLeft : ?

==Details==
{| class="wikitable"
|-
! tagID !! tagName
|-
| 1 || Group
|-
| 41 || PvP
|-
| 62 || Raid
|-
| 81 || Dungeon
|-
| 83 || Legendary
|-
| 85 || Heroic
|-
| 98 || Scenario
|-
| 102 || Account
|-
| 117 || Leatherworking World Quest
|}

:;worldQuestTypes:LE_QUEST_TAG_TYPE_PVP, LE_QUEST_TAG_TYPE_PET_BATTLE, LE_QUEST_TAG_TYPE_PROFESSION, LE_QUEST_TAG_TYPE_DUNGEON
:;rarity:LE_WORLD_QUEST_QUALITY_COMMON, LE_WORLD_QUEST_QUALITY_RARE, LE_WORLD_QUEST_QUALITY_EPIC
(source: FrameXML/WorldMapFrame.lua)

==Patch changes==
* {{Patch 7.0.3|note=New returns for handling World Quests}}
* {{Patch 6.0.2|note=Added.}}

==See also==
{{api|GetQuestLogTitle}}
```