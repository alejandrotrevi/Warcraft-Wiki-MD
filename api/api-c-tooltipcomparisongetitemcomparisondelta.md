# API C TooltipComparison.GetItemComparisonDelta

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TooltipComparison|system=TooltipComparison}}
Needs summary.
 lines = C_TooltipComparison.GetItemComparisonDelta(comparisonItem, equippedItem [, pairedItem, addPairedStats])

==Arguments==
:;comparisonItem:{{apitype|TooltipComparisonItem}}
:;equippedItem:{{apitype|TooltipComparisonItem}}
:;pairedItem:{{apitype|TooltipComparisonItem?}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| guid || {{apitype|WOWGUID}} || 
|}
:;addPairedStats:{{apitype|boolean?}} - Whether the paired item's stats are added or subtracted

==Returns==
:;lines:{{apitype|string[]}}
```