# API C TooltipComparison.GetItemComparisonInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TooltipComparison|system=TooltipComparison}}
Needs summary.
 info = C_TooltipComparison.GetItemComparisonInfo(comparisonItem)

==Arguments==
:;comparisonItem:{{apitype|TooltipComparisonItem}}

==Returns==
:;info:{{apitype|TooltipItemComparisonInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| method || {{apitype|Enum.TooltipComparisonMethod?|default=Single}} || 
|-
| item || {{apitype|TooltipComparisonItem}} || 
|-
| additionalItems || {{apitype|TooltipComparisonItem[]}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.TooltipComparisonMethod
! Value !! Field !! Description
|-
| 0 || Single || 
|-
| 1 || WithBothHands || 
|-
| 2 || WithBagMainHandItem || 
|-
| 3 || WithBagOffHandItem || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ TooltipComparisonItem
! Field !! Type !! Description
|-
| guid || {{apitype|WOWGUID}} || 
|}
```