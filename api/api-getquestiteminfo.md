# API GetQuestItemInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a required/reward/choice quest item.
 name, texture, count, quality, isUsable, itemID = GetQuestItemInfo(type, index)

==Arguments==
:;type:{{apitype|string}} - type of the item to query. One of the following values:
::* "required": Items the quest requires the player to gather.
::* "reward": Unconditional quest rewards.
::* "choice": One of the possible quest rewards.
:;index:{{apitype|number}} - index of the item of the specified type to return information about, ascending from 1.

==Returns==
:;name:{{apitype|string}} - The item's name.
:;texture:{{apitype|number}} : [[FileID]] - The item's icon texture.
:;count:{{apitype|number}} - Amount of the item required or awarded by the quest.
:;quality:{{apitype|Enum.ItemQuality}}
:;isUsable:{{apitype|boolean}} - True if the quest item is usable by the current player.
:;itemID:{{apitype|number}} - The item's ID.

==Details==
* This function returns information about the ''current quest'': the one for which the <code>QUEST_*</code> family of events has fired most recently. Quests in the quest log use {{api|GetQuestLogRewardInfo}} and {{api|GetQuestLogChoiceInfo}}.

==Patch changes==
* {{Patch 9.0.2|note=Added <code>itemID</code> return.<sup>[https://github.com/Gethe/wow-ui-source/commit/fce908e8e7072e64c2c22ac948a5198f415249e2#diff-e6a4dd44b4fb67440f3d93d90433693e22fb4930c6c0a17afdca6857a0b94b1eL446]</sup>}}

==See also==
* {{api|GetNumQuestChoices}}
* {{api|GetNumQuestRewards}}
```