# API GetAvailableQuestInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an available quest.
 isTrivial, frequency, isRepeatable, isLegendary, questID, isImportant = GetAvailableQuestInfo(index)

==Arguments==
:;index:{{apitype|number}} - Index of the available quest to query, starting from 1.

==Returns==
:;isTrivial:{{apitype|boolean}} - true if the quest is trivial (too low-level compared to the character), false otherwise.
:;frequency:{{apitype|number}} - 1 if the quest is a normal quest, <code>LE_QUEST_FREQUENCY_DAILY</code> (2) for daily quests, <code>LE_QUEST_FREQUENCY_WEEKLY</code> (3) for weekly quests.
:;isRepeatable:{{apitype|boolean}} - true if the quest is repeatable, false otherwise.
:;isLegendary:{{apitype|boolean}} - true if the quest is a legendary quest, false otherwise.
:;questID:{{apitype|number}} - quest ID of the quest.
:;isImportant:{{apitype|boolean}} - true if the quest is considered important, false otherwise.

==Patch changes==
* {{Patch 11.0.2|note=Added <code>isImportant</code> return value.<ref>{{ref FrameXML|Blizzard_UIPanels_Game/QuestFrame.lua|11.0.2|55399|372|2024-07-03}}</ref>}}
* {{Patch 9.0.1|note=Added <code>questID</code> return value.<ref>{{ref FrameXML|QuestFrame.lua|9.0.1|36230|363|2020-10-13}}</ref>}}
* {{Patch 6.0.2|note=Changed 1/nil return values to boolean. Changed <code>isDaily</code> return value to <code>frequency</code>.}}
* {{Patch 5.0.4|note=Added <code>isLegendary</code> return value.}}
* {{Patch 3.3.3|note=Added.}}

==References==
{{Reflist}}
```