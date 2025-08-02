# API C PartyInfo.GetMinItemLevel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PartyInfo|system=PartyInfo}}
Needs summary.
 minItemLevel, playerNameWithLowestItemLevel = C_PartyInfo.GetMinItemLevel(avgItemLevelCategory)

==Arguments==
:;avgItemLevelCategory:{{apitype|Enum.AvgItemLevelCategories}} - The active party is always used
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || Base || 
|-
| 1 || EquippedBase || 
|-
| 2 || EquippedEffective || 
|-
| 3 || PvP || 
|-
| 4 || PvPWeighted || 
|-
| 5 || EquippedEffectiveWeighted || 
|}

==Returns==
:;minItemLevel:{{apitype|number}}
:;playerNameWithLowestItemLevel:{{apitype|string}}
```