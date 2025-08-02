# API LootSlotHasItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether a loot slot contains an item.
 isLootItem = LootSlotHasItem(lootSlot)

==Arguments==
:;lootSlot:{{apitype|number}} - index of the loot slot, ascending from 1 to {{api|GetNumLootItems}}()

==Returns==
:;isLootItem:{{apitype|boolean}} - true if the loot slot contains an item rather than coin.

==Example==
Iterate through the items in the currently opened loot window an display them in the chat frame, side by side.
 local itemLinkText
 for i = 1, GetNumLootItems() do
     if (LootSlotHasItem(i)) then
          local iteminfo = GetLootSlotLink(i);
          if itemLinkText == nil then
               itemLinkText = iteminfo
          else
               itemLinkText = itemLinkText .. ", " .. iteminfo
          end
     end
 end
 print(itemLinkText)

==Patch changes==
* {{Patch 5.0.4|note=Renamed from <code>LootSlotIsItem</code> to <code>LootSlotHasItem</code>.}}
```