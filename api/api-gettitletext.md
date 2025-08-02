# API GetTitleText

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of the quest at the quest giver.
 title = GetTitleText()

==Returns==
:;title:{{apitype|string}} - name of the offered quest, e.g. "Inside the Frozen Citadel".

==Details==
* Quest title is updated when the {{api|QUEST_DETAIL|t=e}} event fires.
```