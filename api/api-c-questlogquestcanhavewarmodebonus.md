# API C QuestLog.QuestCanHaveWarModeBonus

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Tests whether a quest is eligible for warmode bonuses (e.g. many world quests).
 hasBonus = C_QuestLog.QuestCanHaveWarModeBonus(questID)

==Arguments==
:;questID:{{apitype|number}} - Unique identifier for a quest, corresponding to the middle portion of a [[QuestString]]

==Returns==
:;hasBonus:{{apitype|boolean}} - True if the quest offers increased rewards to players who maintained warmode during the entire period of completing the quest.

==Patch changes==
* {{Patch 8.3.0|note=Added. (Build 33369, Feb 13 2020)}}
```