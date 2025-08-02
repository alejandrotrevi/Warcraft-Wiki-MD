# API AddAutoQuestPopUp

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Adds a notification to the ObjectiveTrackerFrame that a quest is available or completed.
 AddAutoQuestPopUp(questID, type)

==Arguments==
:;questID:{{apitype|number}} - the quest id
:;type:{{apitype|string}} - popup type, one of "OFFER" or "COMPLETE"

==Example==
 AddAutoQuestPopUp(13222, "OFFER")
```