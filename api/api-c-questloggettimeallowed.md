# API C QuestLog.GetTimeAllowed

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns the time available to complete a quest.
 totalTime, elapsedTime = C_QuestLog.GetTimeAllowed(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;totalTime:{{apitype|number}}
:;elapsedTime:{{apitype|number}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}

==See also==
* {{api|t=a|GetQuestLogTimeLeft}}()
```