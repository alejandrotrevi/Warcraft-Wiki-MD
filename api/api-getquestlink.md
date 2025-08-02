# API GetQuestLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a link for a quest.
 questLink = GetQuestLink(questID)

==Arguments==
:;questID:{{apitype|number}} - Unique identifier for a quest.

==Returns==
:;questLink:{{apitype|string}} - The [[QuestLink|link]] to the quest specified. Returns nil if the QuestID is invalid or if the specified QuestID is not currently in the player's quest log.

==Patch changes==
At an unknown point between patches 6.2 and 7.3.2, this function's argument was changed to take a QuestID instead of a quest log index.
```