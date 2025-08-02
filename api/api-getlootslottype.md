# API GetLootSlotType

**Contributor:** ILeClerk

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns an integer loot type for a given loot slot.
 slotType = GetLootSlotType(slotIndex)

==Arguments==
:;slotIndex:{{apitype|number}} - Position in loot window to query, from 1 - {{api|GetNumLootItems}}().

==Returns==
:;slotType:{{apitype|number}} - Type ID indicating slot content type:
:* 0: <code>LOOT_SLOT_NONE</code> / <code>Enum.LootSlotType.None</code> - No contents
:* 1: <code>LOOT_SLOT_ITEM</code> / <code>Enum.LootSlotType.Item</code> - A regular item
:* 2: <code>LOOT_SLOT_MONEY</code> / <code>Enum.LootSlotType.Money</code> - [[Money|Gold/silver/copper coin]]
:* 3: <code>LOOT_SLOT_CURRENCY</code> / <code>Enum.LootSlotType.Currency</code> - Other currency amount, such as [[Valor Points]]
<p>As of 10.0.0.46455 the constants LOOT_SLOT_NONE, LOOT_SLOT_ITEM, LOOT_SLOT_MONEY, LOOT_SLOT_CURRENCY are no longer defined. A new enumerator table is defined (Enum.LootSlotType) with the same values.

==Example==
The following snippet takes all items from the open loot window, leaving other loot types:
 for slot = 1, GetNumLootItems() do
  if GetLootSlotType(slot) == Enum.LootSlotType.Item then
   LootSlot(slot);
  end
 end

==See also==
*{{api|GetNumLootItems}}
*{{api|LootSlot}}
*{{api|t=e|LOOT_OPENED}}
```