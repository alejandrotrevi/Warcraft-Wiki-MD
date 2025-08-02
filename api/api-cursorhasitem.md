# API CursorHasItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the cursor currently holds an item.
 hasItem = CursorHasItem()

==Returns==
:;hasItem:{{apitype|boolean}} - Whether the cursor is holding an item.

==Details==
This function returns nil if the item on the cursor was not picked up via [[API_PickupContainerItem|PickupContainerItem]], e.g. items from the guild bank (which are picked up via [[API_PickupGuildBankItem|PickupGuildBankItem]]) or a merchant item.
```