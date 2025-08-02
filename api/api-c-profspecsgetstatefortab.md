# API C ProfSpecs.GetStateForTab

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ProfSpecs|system=ProfessionSpecUI}}
Needs summary.
 tabInfo = C_ProfSpecs.GetStateForTab(tabTreeID, configID)

==Arguments==
:;tabTreeID:{{apitype|number}}
:;configID:{{apitype|number}}

==Returns==
:;tabInfo:{{apitype|Enum.ProfessionsSpecTabState}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || Locked || 
|-
| 1 || Unlocked || 
|-
| 2 || Unlockable || 
|}
```