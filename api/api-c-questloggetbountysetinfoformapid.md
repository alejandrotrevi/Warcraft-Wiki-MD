# API C QuestLog.GetBountySetInfoForMapID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_QuestLog|system=QuestLog}}
Returns the bounty set for a specified map ID.
 displayLocation, lockQuestID, bountySetID, isActivitySet = C_QuestLog.GetBountySetInfoForMapID(uiMapID)

==Arguments==
:;uiMapID:{{apitype|number}}

==Returns==
:;displayLocation:{{apitype|Enum.MapOverlayDisplayLocation}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || Default || 
|-
| 1 || BottomLeft || 
|-
| 2 || TopLeft || 
|-
| 3 || BottomRight || 
|-
| 4 || TopRight || 
|-
| 5 || Hidden || 
|}
:;lockQuestID:{{apitype|number}}
:;bountySetID:{{apitype|number}}
:;isActivitySet:{{apitype|boolean}}

==Patch changes==
* {{Patch 10.0.2|note=Addedto <code>isActivitySet</code> return.}}
* {{Patch 9.0.1|note=Moved to <code>C_QuestLog.GetBountySetInfoForMapID()</code>}}
* {{Patch 7.0.3|note=Added as <code>GetQuestBountyInfoForMapID()</code>}}
```