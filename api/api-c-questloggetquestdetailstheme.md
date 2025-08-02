# API C QuestLog.GetQuestDetailsTheme

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns the visual QuestTheme associated with a given quest.
 theme = C_QuestLog.GetQuestDetailsTheme(questID)

==Arguments==
:;questID:{{apitype|number}}

==Returns==
:;theme:{{apitype|QuestTheme?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| background || {{apitype|string}} || 
|-
| seal || {{apitype|string}} || 
|-
| signature || {{apitype|string}} || 
|-
| poiIcon || {{apitype|string}} || 
|}

==Patch changes==
* {{Patch 9.1.0|note=Added <code>poiIcon</code> field.}}
* {{Patch 9.0.1|note=Added.}}
```