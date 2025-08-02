# API GetAbandonQuestName

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of a quest that will be abandoned if {{api|AbandonQuest}} is called.
 questName = GetAbandonQuestName()

==Returns==
:;questName:{{apitype|string}} - Name of the quest that will be abandoned.

==Details==
* The FrameXML-provided quest log calls {{api|SetAbandonQuest}} whenever a quest entry is selected, so this function will usually return the name of the currently selected quest.

==See Also==
* {{api|SetAbandonQuest}}
* {{api|AbandonQuest}}
```