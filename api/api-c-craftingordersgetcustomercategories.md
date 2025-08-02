# API C CraftingOrders.GetCustomerCategories

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CraftingOrders|system=CraftingOrderUI}}
Needs summary.
 categories = C_CraftingOrders.GetCustomerCategories()

==Returns==
:;categories:{{apitype|CraftingOrderCustomerCategory[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| categoryName || {{apitype|string}} || 
|-
| categoryID || {{apitype|number}} || 
|-
| uiSortOrder || {{apitype|number}} || 
|-
| primaryCategorySortOrder || {{apitype|number?}} || 
|-
| secondaryCategorySortOrder || {{apitype|number?}} || 
|-
| type || {{apitype|Enum.CraftingOrderCustomerCategoryType}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.CraftingOrderCustomerCategoryType
! Value !! Field !! Description
|-
| 0 || Primary || 
|-
| 1 || Secondary || 
|-
| 2 || Tertiary || 
|}
```