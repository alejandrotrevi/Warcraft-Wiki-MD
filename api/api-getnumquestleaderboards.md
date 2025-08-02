# API GetNumQuestLeaderBoards

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of objectives for a quest.
 numObjectives = GetNumQuestLeaderBoards([questID])

==Arguments==
:;questID:{{apitype|number?}} - Identifier of the quest. If not provided, default to the currently selected Quest, via [[API SelectQuestLogEntry|SelectQuestLogEntry()]].

==Returns==
:;numObjectives:{{apitype|number}} - The number of objectives this quest possesses (Can be 0).

==Details==
Previous versions of this page stated that the function returns three values, but did not list what the other two values were.
```