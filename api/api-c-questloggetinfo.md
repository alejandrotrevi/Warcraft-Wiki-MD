# API C QuestLog.GetInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns information about a quest in the player's quest log.
 info = C_QuestLog.GetInfo(questLogIndex)

==Arguments==
:;questLogIndex:{{apitype|number}}

==Returns==
:;info:{{apitype|QuestInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|title}} || {{apitype|string}} || The title of the quest
|-
| {{apiname|questLogIndex}} || {{apitype|number}} || 
|-
| {{apiname|questID}} || {{apitype|number}} || 
|-
| {{apiname|campaignID}} || {{apitype|number?}} || 
|-
| {{apiname|level}} || {{apitype|number}} || The level of the quest
|-
| {{apiname|difficultyLevel}} || {{apitype|number}} || 
|-
| {{apiname|suggestedGroup}} || {{apitype|number}} || If designed for more than one player, the number of players suggested to complete the quest.<br>Otherwise, it is 0
|-
| {{apiname|frequency}} || {{apitype|Enum.QuestFrequency?}} || 
|-
| {{apiname|isHeader}} || {{apitype|boolean}} || Whether the entry is a header
|-
| {{apiname|useMinimalHeader}} || {{apitype|boolean}} || <font color="green">10.0.2</font>
|-
| {{apiname|sortAsNormalQuest}} || {{apitype|boolean}} || <font color="green">11.0.2</font>
|-
| {{apiname|isCollapsed}} || {{apitype|boolean}} || Whether the entry is a collapsed header
|-
| {{apiname|startEvent}} || {{apitype|boolean}} || 
|-
| {{apiname|isTask}} || {{apitype|boolean}} || 
|-
| {{apiname|isBounty}} || {{apitype|boolean}} || 
|-
| {{apiname|isStory}} || {{apitype|boolean}} || 
|-
| {{apiname|isScaling}} || {{apitype|boolean}} || 
|-
| {{apiname|isOnMap}} || {{apitype|boolean}} || 
|-
| {{apiname|hasLocalPOI}} || {{apitype|boolean}} || 
|-
| {{apiname|isHidden}} || {{apitype|boolean}} || Whether the quest is not visible inside the player's quest log
|-
| {{apiname|isAutoComplete}} || {{apitype|boolean}} || 
|-
| {{apiname|overridesSortOrder}} || {{apitype|boolean}} || 
|-
| {{apiname|readyForTranslation}} || {{apitype|boolean?|default=true}} || 
|-
| {{apiname|isInternalOnly}} || {{apitype|boolean}} || 
|-
| {{apiname|isAbandonOnDisable}} || {{apitype|boolean}} || <font color="green">10.2.7</font>
|-
| {{apiname|headerSortKey}} || {{apitype|number?}} || <font color="green">11.0.0</font>
|-
| {{apiname|questClassification}} || {{apitype|Enum.QuestClassification}} || <font color="green">11.0.2</font>
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.QuestFrequency
! Value !! Field !! Description
|-
| 0 || {{apiname|Default}} || 
|-
| 1 || {{apiname|Daily}} || 
|-
| 2 || {{apiname|Weekly}} || 
|-
| 3 || {{apiname|ResetByScheduler}} || <font color="green">11.0.0</font>
|}

{{:Enum.QuestClassification}}

==Patch changes==
* {{Patch 11.0.2|note=Removed <code>isLegendarySort</code> field.}}
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.GetInfo()</code>}}
* {{Patch 1.0.0|note=Added as {{api|GetQuestLogTitle}}()}}
```