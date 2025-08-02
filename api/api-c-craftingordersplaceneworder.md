# API C CraftingOrders.PlaceNewOrder

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CraftingOrders|system=CraftingOrderUI}}
Needs summary.
 C_CraftingOrders.PlaceNewOrder(orderInfo)

==Arguments==
:;orderInfo:{{apitype|NewCraftingOrderInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| skillLineAbilityID || {{apitype|number}} || 
|-
| orderType || {{apitype|Enum.CraftingOrderType}} || 
|-
| orderDuration || {{apitype|Enum.CraftingOrderDuration}} || 
|-
| tipAmount || {{apitype|number}} || Commission amount in copper
|-
| customerNotes || {{apitype|string}} || The note to the crafter
|-
| reagentItems || {{apitype|RegularReagentInfo[]}} || Normal reagent items without any quality
|-
| craftingReagentItems || {{apitype|CraftingReagentInfo[]}} || Reagent items that have a reagent quality
|-
| minCraftingQualityID || {{apitype|number?}} || 
|-
| orderTarget || {{apitype|string?}} || The player name for a personal order
|-
| recraftItem || {{apitype|string?}} || 
|}

{{:Enum.CraftingOrderType}}

{{:Enum.CraftingOrderDuration}}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ RegularReagentInfo
! Field !! Type !! Description
|-
| itemID || {{apitype|number}} || 
|-
| quantity || {{apitype|number}} || 
|}

{{:Struct CraftingReagentInfo}}

==Example==
Posts a public work order for [[Shock-Spring Coil]] while providing all the materials.
<syntaxhighlight lang="lua">
local info = {
    skillLineAbilityID = 47446, -- Shock-Spring Coil
    orderType = Enum.CraftingOrderType.Public,
    orderDuration = Enum.CraftingOrderDuration.Short,
    tipAmount = 100,
    customerNotes = "",
    reagentItems = { -- leave this table empty to omit reagents
        {
            quantity = 2,
            itemID = 190315, -- Rousing Earth
            dataSlotIndex = 1,
        },
    },
    craftingReagentItems = { -- leave this table empty to omit reagents
        {
            quantity = 6,
            itemID = 198183, -- Handful of Serevite Bolts
            dataSlotIndex = 1,
        },
    },
}

C_CraftingOrders.PlaceNewOrder(info)
</syntaxhighlight>
```