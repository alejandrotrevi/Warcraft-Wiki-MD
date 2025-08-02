# API GetQuestLogSpecialItemCooldown

**Contributor:** DokoNinjaroboto

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns cooldown information about a special quest item based on a given index
 start, duration, enable = GetQuestLogSpecialItemCooldown(questLogIndex)

==Arguments==
:;questLogIndex:{{apitype|number}} - The index of the quest to query. The number of quests can be retrieved with {{api|GetNumQuestLogEntries}}()

==Returns==
:;start:{{apitype|number}} - The value of GetTime() when the quest items's cooldown began (or <code>0</code> if the item is off cooldown).
:;duration:{{apitype|number}} - The duration of the items's cooldown (is <code>0</code> if the item is ready).
:;enable:{{apitype|number}} - <code>1</code> if the item is enabled, otherwise <code>0</code> (needs verification)
```