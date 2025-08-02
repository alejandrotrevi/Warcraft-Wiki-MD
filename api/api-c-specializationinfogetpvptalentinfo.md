# API C SpecializationInfo.GetPvpTalentInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpecializationInfo|system=SpecializationInfo}}
Needs summary.
 talentInfo = C_SpecializationInfo.GetPvpTalentInfo(talentID)

==Arguments==
:;talentID:{{apitype|number}}

==Returns==
:;talentInfo:{{apitype|PvpTalentInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| talentID || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| icon || {{apitype|number}} || 
|-
| selected || {{apitype|boolean}} || 
|-
| available || {{apitype|boolean}} || 
|-
| spellID || {{apitype|number}} || 
|-
| unlocked || {{apitype|boolean}} || 
|-
| known || {{apitype|boolean}} || 
|-
| grantedByAura || {{apitype|boolean}} || 
|-
| dependenciesUnmet || {{apitype|boolean}} || 
|-
| dependenciesUnmetReason || {{apitype|string?}} || 
|}
```