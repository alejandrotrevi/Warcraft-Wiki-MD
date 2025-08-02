# API IsBattlePayItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether an item was purchased from the in-game store.
 isPayItem = IsBattlePayItem(bag, slot)

==Arguments==
:;bag:{{apitype|number}} ([[bagID]]) - container ID, e.g. 0 for backpack.
:;slot:{{apitype|number}} - slot index within the container, ascending from 1.

==Returns==
:;isPayItem:{{apitype|boolean}} - true if the item was purchased from the in-game store, false otherwise.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}
```