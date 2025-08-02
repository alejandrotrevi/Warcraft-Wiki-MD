# API C LegendaryCrafting.GetRuneforgePowerInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LegendaryCrafting|system=LegendaryCrafting}}
Needs summary.
 power = C_LegendaryCrafting.GetRuneforgePowerInfo(runeforgePowerID)

==Arguments==
:;runeforgePowerID:{{apitype|number}}

==Returns==
:;power:{{apitype|RuneforgePower}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| runeforgePowerID || {{apitype|number}} || 
|-
| state || {{apitype|Enum.RuneforgePowerState}} || 
|-
| name || {{apitype|string}} || 
|-
| descriptionSpellID || {{apitype|number}} || 
|-
| description || {{apitype|string}} || 
|-
| source || {{apitype|string?}} || 
|-
| iconFileID || {{apitype|number}} || 
|-
| specName || {{apitype|string?}} || 
|-
| matchesSpec || {{apitype|boolean}} || 
|-
| matchesCovenant || {{apitype|boolean}} || 
|-
| covenantID || {{apitype|number?}} || 
|-
| slots || {{apitype|string[]}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.RuneforgePowerState
! Value !! Field !! Description
|-
| 0 || Available || 
|-
| 1 || Unavailable || 
|-
| 2 || Invalid || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```