# API C CraftingOrders.CalculateCraftingOrderPostingFee

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CraftingOrders|system=CraftingOrderUI}}
Needs summary.
 deposit = C_CraftingOrders.CalculateCraftingOrderPostingFee(skillLineAbilityID, orderType, orderDuration)

==Arguments==
:;skillLineAbilityID:{{apitype|number}}
:;orderType:{{apitype|Enum.CraftingOrderType}}
{{:Enum.CraftingOrderType|nocaption=1}}
:;orderDuration:{{apitype|Enum.CraftingOrderDuration}}
{{:Enum.CraftingOrderDuration|nocaption=1}}

==Returns==
:;deposit:{{apitype|number}}
```