# API GetQuestCurrencyInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}

Returns information about a currency token rewarded from the quest currently being viewed in the quest info frame.

 name, texture, numItems, quality = GetQuestCurrencyInfo(itemType, index)

==Arguments==

:;itemType:{{apitype|string}} - The category of the currency to query. Currently "reward" is the only category in use for currencies.
:;index:{{apitype|number}} - The index of the currency to query, in the range [1,[[API_GetNumRewardCurrencies|GetNumRewardCurrencies()]]].

==Returns==

:;name:{{apitype|string}} - The localized name of the currency.
:;texture:{{apitype|string}} - The path to the icon texture used for the currency.
:;numItems:{{apitype|number}} - The amount of the currency that will be rewarded.
:;quality:{{apitype|number}} - Indicates the rarity of the currency.

==Details==

This function does not work for quests being viewed from the player's quest log. Use {{api|GetQuestLogRewardCurrencyInfo}} instead. Check ''QuestInfoFrame.questLog'' to determine whether the quest info frame is currently displaying a quest log quest or not.

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

==See also==

* {{api|GetNumRewardCurrencies}}
* {{api|GetQuestLogRewardCurrencyInfo}}
```