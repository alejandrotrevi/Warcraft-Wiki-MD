# API GetLootSourceInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the source of the objects in a loot slot.
 guid, quantity, ... = GetLootSourceInfo(lootSlot)

==Arguments==
:;lootSlot:{{apitype|number}} - index of the loot slot, ascending from 1 up to {{api|GetNumLootItems}}()

==Returns==
(Variable returns: <code>guid1, quantity1, guid2, quantity2, ...</code>)
:;guid:{{apitype|string}} - [[GUID#Creature|GUID]] of the source being looted. Can also return <code>GameObject</code> guids for objects like ore veins and herbs, and [[GUID#Item|Item]] guids for containers like lockboxes.
:;quantity:{{apitype|number}} - Quantity of the object being looted from this source.

==Example==
Prints out the source guid and quantity of each loot source item individually.
<syntaxhighlight lang="lua">
local function OnEvent(self, event)
	for i = 1, GetNumLootItems() do
		local sources = {GetLootSourceInfo(i)}
		local _, name = GetLootSlotInfo(i)
		for j = 1, #sources, 2 do
			print(i, name, j, sources[j], sources[j+1])
		end
	end
end

local f = CreateFrame("Frame")
f:RegisterEvent("LOOT_OPENED")
f:SetScript("OnEvent", OnEvent)
</syntaxhighlight>
[[File:API_GetLootSourceInfo.png]]

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|GetLootSlotInfo}}()
```