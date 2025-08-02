# API GetQuestGreenRange

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Return for how many levels below you quests and mobs remain "green" (i.e. yield xp)
 range = GetQuestGreenRange()

==Parameters==

===Returns===

:;range:{{apitype|number}} - an integer value, currently up to 12 (at level 60)

==Example==

* At level 9, GetQuestGreenRange() returns '''5'''

* At level 50, GetQuestGreenRange() returns '''10'''
```