# API QuestGetAutoAccept

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the last-offered quest was automatically accepted.
 isAutoAccepted = QuestGetAutoAccept()

==Returns==
:;isAutoAccepted:{{apitype|boolean}} - true if the last-offered quest was automatically accepted; false if the player has to accept it using {{api|AcceptQuest}}().

==Details==
* Automatically-accepted quests are common in starting areas since [[Patch 3.3.0]]: simply opening the quest description is sufficient to accept the quest.

==Patch changes==
* Added in [[Patch 3.3.0]]
```