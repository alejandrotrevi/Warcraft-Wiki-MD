# API GetQuestSortIndex

**Contributor:** DokoNinjaroboto

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index of the collapsible category the queried quest belongs to
 sortIndex = GetQuestSortIndex(questLogIndex)

==Arguments==
:;questLogIndex:{{apitype|number}} - The index of the quest to query. The number of quests can be retrieved with {{api|GetNumQuestLogEntries}}()

==Returns==
:;sortIndex:{{apitype|number}} - The index of the category starting from <code>1</code>

==Notes==
* Quests are usually split per zone, so if for example there are quests from 5 zones present, '''sortIndex''' will range between <code>1-5</code>
* Querying the category header itself will return the same '''sortIndex''' as the quests it lists
```