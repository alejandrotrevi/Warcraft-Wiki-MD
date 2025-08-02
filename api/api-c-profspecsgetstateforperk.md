# API C ProfSpecs.GetStateForPerk

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ProfSpecs|system=ProfessionSpecUI}}
Needs summary.
 state = C_ProfSpecs.GetStateForPerk(perkID, configID)

==Arguments==
:;perkID:{{apitype|number}}
:;configID:{{apitype|number}}

==Returns==
:;state:{{apitype|Enum.ProfessionsSpecPerkState}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || Unearned || 
|-
| 1 || Pending || 
|-
| 2 || Earned || 
|}
```