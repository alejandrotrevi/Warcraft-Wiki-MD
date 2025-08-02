# API C QuestLine.GetQuestLineInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLine|system=QuestLineUI}}
Needs summary.
 questLineInfo = C_QuestLine.GetQuestLineInfo(questID [, uiMapID [, displayableOnly]])

==Arguments==
:;questID:{{apitype|number}}
:;uiMapID:{{apitype|number?}} : [[UiMapID]]
:;displayableOnly:{{apitype|boolean?|default=false}}

==Returns==
:;questLineInfo:{{apitype|QuestLineInfo?}}
{{:Struct QuestLineInfo|nocaption=1}}

==Patch changes==
* {{Patch 11.0.0|note=Added <code>displayableOnly</code> argument.}}
* {{Patch 8.0.1|note=Added.}}
```