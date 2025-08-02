# API UseInventoryItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent}}
Use an item in a specific inventory slot.
 UseInventoryItem(slot)

==Arguments==
:;slot:{{apitype|number}} - The inventory [[API TYPE InventorySlotID|slot ID]]

==Patch changes==
: After patch 1.6 you cant auto-use items anymore. Addons can no longer activate items without the press of a button. In order to use UseInventoryItem( GetInventorySlotInfo("Trinket0Slot") ) you will have to call it from a button, keypress or icon as you do with spells.
```