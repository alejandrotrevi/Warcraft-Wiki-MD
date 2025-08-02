# API C SpecializationInfo.GetPvpTalentSlotInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpecializationInfo|system=SpecializationInfo}}
Needs summary.
 slotInfo = C_SpecializationInfo.GetPvpTalentSlotInfo(talentIndex)

==Arguments==
:;talentIndex:{{apitype|number}}

==Returns==
:;slotInfo:{{apitype|PvpTalentSlotInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| enabled || {{apitype|boolean}} || 
|-
| level || {{apitype|number}} || 
|-
| selectedTalentID || {{apitype|number?}} || 
|-
| availableTalentIDs || {{apitype|number[]}} || 
|}

==Patch changes==
* {{Patch 8.2.5|note=Added <code>level</code> field.}}
* {{Patch 8.0.1|note=Added.}}
```