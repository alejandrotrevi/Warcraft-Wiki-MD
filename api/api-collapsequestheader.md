# API CollapseQuestHeader

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Collapses a quest log header.
 CollapseQuestHeader(index [, isAuto])

==Arguments==
:;index:{{apitype|number}} - Position in the quest log from 1 at the top, including collapsed and invisible content.
:;isAuto:{{apitype|boolean}} - Used when resetting the quest log to a default state.

==Example==
Collapse the first quest header (always at position 1) while suppressing the normal event handler:
<syntaxhighlight lang="lua">
QuestMapFrame.ignoreQuestLogUpdate = true
CollapseQuestHeader(1)
QuestMapFrame.ignoreQuestLogUpdate = nil
</syntaxhighlight>
```