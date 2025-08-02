# API C CraftingOrders.ListMyOrders

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CraftingOrders|system=CraftingOrderUI}}
Needs summary.
 C_CraftingOrders.ListMyOrders(request)

==Arguments==
:;request:{{apitype|CraftingOrderRequestMyOrdersInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| primarySort || {{apitype|CraftingOrderSortInfo}} || 
|-
| secondarySort || {{apitype|CraftingOrderSortInfo}} || 
|-
| offset || {{apitype|number}} || 
|-
| callback || {{apitype|CraftingOrderRequestMyOrdersCallback}} || 
|}

{{:Struct CraftingOrderSortInfo}}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ CraftingOrderRequestMyOrdersCallback
! !! Param !! Type !! Description
|-
| 1 || result|| {{apitype|Enum.CraftingOrderResult}} || [[Enum.CraftingOrderResult]]
|-
| 2 || expectMoreRows|| {{apitype|booleane}} || 
|-
| 3 || offset|| {{apitype|number}} || 
|-
| 4 || isSorted|| {{apitype|boolean}} || 
|}
```