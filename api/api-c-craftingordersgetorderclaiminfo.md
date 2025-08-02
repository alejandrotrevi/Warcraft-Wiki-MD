# API C CraftingOrders.GetOrderClaimInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CraftingOrders|system=CraftingOrderUI}}
Needs summary.
 claimInfo = C_CraftingOrders.GetOrderClaimInfo(profession)

==Arguments==
:;profession:{{apitype|Enum.Profession}}
{{:Enum.Profession|nocaption=1}}

==Returns==
:;claimInfo:{{apitype|CraftingOrderClaimsRemainingInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| claimsRemaining || {{apitype|number?|default=0}} || 
|-
| hoursToRecharge || {{apitype|number?}} || 
|}
```