# API GetItemCount

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns the number (or available charges) of an item in the inventory.
 count = GetItemCount(itemInfo [, includeBank, includeUses, includeReagentBank])

==Arguments==
:;itemInfo:{{apitype|number,string}} - {{:ItemInfo}}
:;includeBank:{{apitype|boolean?}} - If true, includes the bank
:;includeUses:{{apitype|boolean?}} - If true, includes each charge of an item similar to {{api|GetActionCount()}}
:;includeReagentBank:{{apitype|boolean?}} - If true, includes the reagent bank

==Returns==
:;count:{{apitype|number}} - The number of items in your possession, or charges if includeUses is true and the item has charges.

==Example==
<syntaxhighlight lang="lua">
local count = GetItemCount(29434)
print("Badge of Justice:", count)

local count = GetItemCount(33312, nil, true) 
print("Mana Saphire Charges:", count)

local clothInBags = GetItemCount("Netherweave Cloth")
local clothInTotal = GetItemCount("Netherweave Cloth", true)
print("Netherweave Cloth:", clothInBags, "(bags)", (clothInTotal - clothInBags), "(bank)")
</syntaxhighlight>

==Patch changes==
* {{Patch 7.2.0|note=Added ''includeReagentBank'' optional argument.<ref>{{ref FrameXML|MerchantFrame.lua|7.2.0|23835|578|2017-03-28}}</ref>}}
* {{Patch 2.3.0|note=Added ''includeUses'' optional argument.<ref>{{ref web|title=Upcoming 2.3 Changes - Concise List|url=http://forums.worldofwarcraft.com/thread.html?topicId=879058320&pageNo=1&sid=1#0|author=[[Iriel]]|date=2007-08-27|archiveurl=http://blue.cardplace.com/newcache/us/879058320.htm|publisher=[[BlueTracker]]}}</ref>}}
* {{Patch 2.0.1|note=Added.<ref>{{ref web|author={{Blizz}}[[slouken]]|title=Re: 2.0.0 Changes - Concise List|date=2006-10-11|url=http://forums.worldofwarcraft.com/thread.html?topicId=15401595&pageNo=32&sid=1#636|archiveurl=http://blue.cardplace.com/newcache/us/15401595.htm}}</ref>}}

==References==
{{Reflist}}
```