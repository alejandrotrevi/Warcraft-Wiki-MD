# API C DelvesUI.GetRoleSubtreeForCompanion

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_DelvesUI|system=DelvesUI}}
Needs summary.
 subTreeID = C_DelvesUI.GetRoleSubtreeForCompanion(companionID?, roleType)

==Arguments==
:;companionID:{{apitype|number?}}
:;roleType:{{apitype|Enum.CompanionRoleType}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || {{apiname|Dps}} || 
|-
| 1 || {{apiname|Heal}} || 
|-
| 2 || {{apiname|Tank}} || 
|}

==Returns==
:;subTreeID:{{apitype|number}}
```