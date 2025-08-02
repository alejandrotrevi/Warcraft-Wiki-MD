# API C QuestLog.GetQuestIDForLogIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Only returns a questID for actual quests, not headers
 questID = C_QuestLog.GetQuestIDForLogIndex(questLogIndex)

==Arguments==
:;questLogIndex:{{apitype|number}}

==Returns==
:;questID:{{apitype|number?}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```