# API AcknowledgeAutoAcceptQuest

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Acknowledges that the currently-offered auto-accept quest has been accepted by the player.
 AcknowledgeAutoAcceptQuest()

==Details==
* Quests flagged for auto-accept are forced into the player's quest log immediately, rendering accepting the quest a mere formality.
* Calling this function allows the server to keep track of whether it should keep trying to get you to accept the quest via autoquest popups.
* You'll acknowledge the last quest for which the {{api|t=e|QUEST_DETAIL}} event fired.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|AcceptQuest}}
* {{api|GetAutoQuestPopUp}}
```