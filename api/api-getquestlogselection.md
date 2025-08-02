# API GetQuestLogSelection

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a number associated with the QuestLogSelection index.
 questSelected = GetQuestLogSelection()

----
;''Arguments''

:''none''

----
;''Returns''

:Number questSelected

:;questSelected:The number for the currently selected quest.

----
;''Example''
 local questSelected = GetQuestLogSelection()
 print(questSelected)

;''Result''
 1

----
;''Description''

: Returns a number associated with the QuestLogSelection index.
```