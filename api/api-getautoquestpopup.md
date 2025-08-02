# API GetAutoQuestPopUp

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns info for a popup quest notification.
 questID, type = GetAutoQuestPopUp(index)

==Arguments==
:;index:{{apitype|number}} - which popup to get information about, between 1 and {{api|GetNumAutoQuestPopUps}}()

==Returns==
:;questID:{{apitype|number}} - the quest id
:;type:{{apitype|string}} - Notification type.  One of "OFFER" (new quest added) or "COMPLETE" (quest finished).

==Patch changes==
* {{Patch 4.0.1|note=Added.}}

==See also==
* {{api|AddAutoQuestPopUp}}
* {{api|GetNumAutoQuestPopUps}}
```