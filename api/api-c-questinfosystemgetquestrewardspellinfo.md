# API C QuestInfoSystem.GetQuestRewardSpellInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestInfoSystem|system=QuestInfoSystem}}
Needs summary.
 info = C_QuestInfoSystem.GetQuestRewardSpellInfo([questID], spellID)

==Arguments==
:;questID:{{apitype|number?}}
:;spellID:{{apitype|number}} - Spell Ids from {{api|C_QuestInfoSystem.GetQuestRewardSpells}}

==Returns==
:;info:{{apitype|QuestRewardSpellInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|texture}} || {{apitype|fileID}} || 
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|garrFollowerID}} || {{apitype|number?}} || 
|-
| {{apiname|isTradeskill}} || {{apitype|boolean}} || 
|-
| {{apiname|isSpellLearned}} || {{apitype|boolean}} || 
|-
| {{apiname|hideSpellLearnText}} || {{apitype|boolean}} || 
|-
| {{apiname|isBoostSpell}} || {{apitype|boolean}} || 
|-
| {{apiname|genericUnlock}} || {{apitype|boolean}} || 
|-
| {{apiname|type}} || {{apitype|Enum.QuestCompleteSpellType}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.QuestCompleteSpellType
! Value !! Field !! Description
|-
| 0 || {{apiname|LegacyBehavior}} || 
|-
| 1 || {{apiname|Follower}} || 
|-
| 2 || {{apiname|Tradeskill}} || 
|-
| 3 || {{apiname|Ability}} || 
|-
| 4 || {{apiname|Aura}} || 
|-
| 5 || {{apiname|Spell}} || 
|-
| 6 || {{apiname|Unlock}} || 
|-
| 7 || {{apiname|Companion}} || 
|-
| 8 || {{apiname|QuestlineUnlock}} || <font color="green">11.0.0</font>
|-
| 9 || {{apiname|QuestlineReward}} || <font color="green">11.0.0</font>
|-
| 10 || {{apiname|QuestlineUnlockPart}} || <font color="green">11.0.0</font>
|-
| 11 || {{apiname|PossibleReward}} || <font color="green">11.2.0</font>
|}
```