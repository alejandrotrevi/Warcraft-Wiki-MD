# API SortQuestWatches

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sorts watched quests by proximity to the player character.
 changed = SortQuestWatches()

==Returns==
:;changed:{{apitype|boolean}} - true if any change to the order of watched quests was made, false otherwise.

==Patch changes==
* {{Patch 7.1.0|note=Fixed sort order.}}
* {{Patch 7.0.3|note=(Bug) sorts quests in reverse order, the closest quests would be at the bottom of the list.}}
* {{Patch 3.3.3|note=Added.}}
```