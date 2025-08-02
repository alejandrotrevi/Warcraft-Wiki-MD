# API ShowQuestComplete

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Shows the completion dialog for a complete, auto-completable quest.
 ShowQuestComplete(questID)

==Arguments==
:;questID:{{apitype|number}} - id of the quest which is complete and auto-completable.

==Triggers events==
* {{api|t=e|QUEST_COMPLETE}}, when completion/reward information is available.

==Details==
* Auto-completable quests can be turned in anywhere in the world, instead of requiring interaction with a specific NPC.

==Patch changes==
* {{Patch 4.0.1|note=Added.}}
```