# API ExpandQuestHeader

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Expands a quest log header.
 ExpandQuestHeader(index [, isAuto])

==Arguments==
:;index:{{apitype|number}} - Position in the quest log from 1 at the top, including collapsed and invisible content.
:;isAuto:{{apitype|boolean}} - Used when resetting the quest log to a default state.

==Details==
* Applies to all headers when the index does not point to a header, inluding out-of-range values like 0.
* Fires {{api|t=e|QUEST_LOG_UPDATE}}.  Toggle <code>QuestMapFrame.ignoreQuestLogUpdate</code> to supress the normal event handler.

==Example==
Expand all quest headers:
<syntaxhighlight lang="lua">
ExpandQuestHeader(0)
</syntaxhighlight>

==Patch changes==
* {{Patch 7.0.3|note=Added ''isAuto'' optional argument.<ref>{{ref FrameXML|QuestMapFrame.lua|7.0.3|22267|212|2016-07-19}}</ref>}}

==See also==
* {{api|QuestMapFrame_ResetFilters}}() - [[FrameXML]] function to restore the default expanded/collapsed state. {{elinks-api/Inline|tly-go=QuestMapFrame_ResetFilters|git-search=QuestMapFrame_ResetFilters}}

==References==
{{Reflist}}
```