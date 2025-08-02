# API GetQuestLogRewardCurrencyInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}

Provides information about a currency reward for the quest currently being viewed in the quest log, or of the provided questId.

 name, texture, numItems, currencyId, quality = GetQuestLogRewardCurrencyInfo(index [, questId])

==Arguments==

:;index:{{apitype|number}} - The index of the currency to query, in the range of [1,[[API_GetNumRewardCurrencies|GetNumRewardCurrencies()]]] or [1, [[API_GetNumQuestLogRewardCurrencies|GetNumQuestLogRewardCurrencies()]]]
:;index:questId - The id of a quest

==Returns==

:;name:{{apitype|string}} - The localized name of the currency
:;texture:{{apitype|string}} - The path to the icon texture used for the currency
:;numItems:{{apitype|number}} - The amount of the currency that will be rewarded
:;currencyId:{{apitype|number}} - The id of the curreny
:;quality:{{apitype|number}} - The quality of the curreny

==Details==

When no questId is provided, this function only works for the quest currently viewed in the quest log.
When a questId is provided, the function will provide information only if the quest reward data is loaded ({{api|t=e|QUEST_LOG_UPDATE}}).
For quests being viewed from NPCs, use {{api|GetQuestCurrencyInfo}} instead. Check ''QuestInfoFrame.questLog'' to determine whether the quest info frame is currently displaying a quest log quest or not.

==Example==

Print a list of currencies rewarded by the currently viewed quest to the chat frame:

 local numRewardCurrencies = GetNumRewardCurrencies()
 if numRewardCurrencies > 0 then
    print("This quest rewards", numRewardCurrencies, "currencies:")
    for i = 1, numRewardCurrencies do
       local name, texture, numItems
       if QuestInfoFrame.questLog then
          name, texture, numItems = GetQuestLogRewardCurrencyInfo(i)
       else
          name, texture, numItems = GetQuestCurrencyInfo("reward", i)
       end
       print(format("\124T%s:0\124t %dx %s", texture, numItems, name))
    end
 else
    print("This quest does not reward any currencies.")
 end

==Patch changes==
* {{Patch 4.0.1|note=Added, effectively replacing functions such as <code>GetQuestLogRewardHonor()</code> and <code>GetQuestLogRewardArenaPoints()</code>.}}

==See also==

* {{api|GetNumQuestCurrencies}}
* {{api|GetNumRewardCurrencies}}
* {{api|GetQuestCurrencyInfo}}
```