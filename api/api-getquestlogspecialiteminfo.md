# API GetQuestLogSpecialItemInfo

**Contributor:** DokoNinjaroboto

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a special quest item based on a given index
 link, item, charges, showItemWhenComplete = GetQuestLogSpecialItemInfo(questLogIndex)

==Arguments==
:;questLogIndex:{{apitype|number}} - The index of the quest to query. The number of quests can be retrieved with {{api|GetNumQuestLogEntries}}()

==Returns==
:;link:{{apitype|string?}} : [[ItemLink]]
:;item:{{apitype|number}} - The icon ID
:;charges:{{apitype|number}} - The number of charges, or <code>0</code> if unlimited. If the item is consumed on use this seems to be <code>-1</code> (e.g., Mana Remnants)
:;showItemWhenComplete:{{apitype|boolean}} - Whether the item remains visible when complete
```