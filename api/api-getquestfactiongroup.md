# API GetQuestFactionGroup

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
 factionGroup = GetQuestFactionGroup(questID)

==Arguments==
:;questID:{{apitype|number}} - Unique [[QuestID]].

==Returns==
:;factionGroup:{{apitype|number}}

{| class="darktable zebra"
|+
!Key
!Value
!Description
|-
|
|0
|Neutral{{fact}} <!-- Is this true?  In the source code, it seems like neutral is just nil. -->
|
|-
|LE_QUEST_FACTION_ALLIANCE
|1
|Alliance
|-
|LE_QUEST_FACTION_HORDE
|2
|Horde
|}

==Patch changes==
* {{Patch 6.0.2|note=Added.<ref>{{ref FrameXML|QuestMapFrame.lua|6.0.2}}</ref>}}

==References==
{{Reflist}}
```