# API ConfirmLootSlot

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Confirms looting of a BoP item.
 ConfirmLootSlot(slot)

==Arguments==
:;slot:{{apitype|number}} - the loot slot of a BoP loot item that is waiting for confirmation

==Details==
If the player has already clicked on a LootButton object with loot index 1, and the item is "Bind on Pickup" and awaiting confirmation, then the item will be looted and placed in the player's bags.
```