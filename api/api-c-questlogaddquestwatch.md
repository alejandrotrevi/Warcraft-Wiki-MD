# API C QuestLog.AddQuestWatch

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Tracks a quest.
 wasWatched = C_QuestLog.AddQuestWatch(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;wasWatched:{{apitype|boolean}}

==Patch changes==
* {{Patch 11.0.0|note=Removed <code>watchType</code> argument.}}
```