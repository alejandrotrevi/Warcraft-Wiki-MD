# API C Garrison.GetTalentInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Garrison|system=GarrisonInfo}}
Needs summary.
 info = C_Garrison.GetTalentInfo(talentID)

==Arguments==
:;talentID:{{apitype|number}} - {{dbc|garrtalent|GarrTalent.ID}}

==Returns==
:;info:{{apitype|GarrisonTalentInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| id || {{apitype|number}} || 
|-
| ability || {{apitype|GarrisonFollowerAbilityInfo}} || 
|-
| name || {{apitype|string}} || 
|-
| icon || {{apitype|number}} || 
|-
| tier || {{apitype|number}} || 
|-
| uiOrder || {{apitype|number}} || 
|-
| type || {{apitype|number}} || 
|-
| prerequisiteTalentID || {{apitype|number?}} || 
|-
| selected || {{apitype|boolean}} || 
|-
| researched || {{apitype|boolean}} || 
|-
| ignoreTalent || {{apitype|boolean}} || 
|-
| researchDuration || {{apitype|number}} || 
|-
| startTime || {{apitype|number}} || 
|-
| timeRemaining || {{apitype|number}} || 
|-
| researchGoldCost || {{apitype|number}} || 
|-
| researchCurrencyCosts || {{apitype|GarrisonTalentCurrencyCostInfo[]}} || 
|-
| talentAvailability || {{apitype|Enum.GarrisonTalentAvailability}} || 
|-
| talentRank || {{apitype|number}} || 
|-
| talentMaxRank || {{apitype|number}} || 
|-
| isBeingResearched || {{apitype|boolean}} || 
|-
| description || {{apitype|string}} || 
|-
| perkSpellID || {{apitype|number}} || 
|-
| researchDescription || {{apitype|string?}} || 
|-
| playerConditionReason || {{apitype|string?}} || 
|-
| socketInfo || {{apitype|GarrisonTalentSocketInfo}} || 
|-
| treeID || {{apitype|number}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ GarrisonFollowerAbilityInfo
! Field !! Type !! Description
|-
| id || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| icon || {{apitype|number}} || 
|-
| isTrait || {{apitype|boolean}} || 
|-
| isSpecialization || {{apitype|boolean}} || 
|-
| temporary || {{apitype|boolean}} || 
|-
| category || {{apitype|string?}} || 
|-
| counters || {{apitype|GarrisonAbilityEffect[]}} || 
|-
| isEmptySlot || {{apitype|boolean}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ GarrisonAbilityEffect
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| icon || {{apitype|number}} || 
|-
| factor || {{apitype|number}} || 
|}

{{:Struct GarrisonTalentCurrencyCostInfo}}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ Enum.GarrisonTalentAvailability
! Value !! Field !! Description
|-
| align="center" | 0 || Available || 
|-
| align="center" | 1 || Unavailable || 
|-
| align="center" | 2 || UnavailableAnotherIsResearching || 
|-
| align="center" | 3 || UnavailableNotEnoughResources || 
|-
| align="center" | 4 || UnavailableNotEnoughGold || 
|-
| align="center" | 5 || UnavailableTierUnavailable || 
|-
| align="center" | 6 || UnavailablePlayerCondition || 
|-
| align="center" | 7 || UnavailableAlreadyHave || 
|-
| align="center" | 8 || UnavailableRequiresPrerequisiteTalent || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ GarrisonTalentSocketInfo
! Field !! Type !! Description
|-
| socketType || {{apitype|number}} || 
|-
| socketSubtype || {{apitype|number}} || 
|-
| misc0 || {{apitype|number}} || 
|-
| misc1 || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 9.2.0|note=Added <code>ignoreTalent, treeID</code> fields.}}
* {{Patch 9.0.1|note=Added.}}
```