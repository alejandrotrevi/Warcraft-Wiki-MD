# API GetNumRewardCurrencies

**Contributor:** Bigsxy

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}

Returns the number of currency rewards for the quest currently being viewed in the quest log or quest info frame.

 numCurrencies = GetNumRewardCurrencies()

==Returns==

:;numCurrencies:{{apitype|number}} - The number of currency rewards

==Details==
This function does not work for quests being viewed from the player's quest log. Use [[API_GetNumQuestLogRewardCurrencies]] instead. Check QuestInfoFrame.questLog to determine whether the quest info frame is currently displaying a quest log quest or not. 

==See also==

* {{api|GetNumQuestRewards}}
* {{api|GetNumQuestChoices}}
* {{api|GetQuestCurrencyInfo}}
* {{api|GetQuestLogRewardCurrencyInfo}}
* {{api|GetNumQuestLogRewardCurrencies}}
```