# API C ProfSpecs.GetStateForPath

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ProfSpecs|system=ProfessionSpecUI}}
Needs summary.
 state = C_ProfSpecs.GetStateForPath(pathID, configID)

==Arguments==
:;pathID:{{apitype|number}}
:;configID:{{apitype|number}}

==Returns==
:;state:{{apitype|Enum.ProfessionsSpecPathState}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || Locked || 
|-
| 1 || Progressing || 
|-
| 2 || Completed || 
|}
```