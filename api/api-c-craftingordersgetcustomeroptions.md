# API C CraftingOrders.GetCustomerOptions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CraftingOrders|system=CraftingOrderUI}}
Needs summary.
 results = C_CraftingOrders.GetCustomerOptions(params)

==Arguments==
:;params:{{apitype|CraftingOrderCustomerSearchParams}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|categoryFilters}} || {{apitype|CraftingOrderCustomerCategoryFilters}} || 
|-
| {{apiname|searchText}} || {{apitype|string?}} || 
|-
| {{apiname|minLevel}} || {{apitype|number}} || 
|-
| {{apiname|maxLevel}} || {{apitype|number}} || 
|-
| {{apiname|uncollectedOnly}} || {{apitype|boolean}} || 
|-
| {{apiname|usableOnly}} || {{apitype|boolean}} || 
|-
| {{apiname|upgradesOnly}} || {{apitype|boolean}} || 
|-
| {{apiname|currentExpansionOnly}} || {{apitype|boolean}} || <font color="green">11.0.0</font>
|-
| {{apiname|includePoor}} || {{apitype|boolean}} || 
|-
| {{apiname|includeCommon}} || {{apitype|boolean}} || 
|-
| {{apiname|includeUncommon}} || {{apitype|boolean}} || 
|-
| {{apiname|includeRare}} || {{apitype|boolean}} || 
|-
| {{apiname|includeEpic}} || {{apitype|boolean}} || 
|-
| {{apiname|includeLegendary}} || {{apitype|boolean}} || 
|-
| {{apiname|includeArtifact}} || {{apitype|boolean}} || 
|-
| {{apiname|isFavoritesSearch}} || {{apitype|boolean}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ CraftingOrderCustomerCategoryFilters
! Field !! Type !! Description
|-
| {{apiname|primaryCategoryID}} || {{apitype|number?}} || 
|-
| {{apiname|secondaryCategoryID}} || {{apitype|number?}} || 
|-
| {{apiname|tertiaryCategoryID}} || {{apitype|number?}} || 
|}

==Returns==
:;results:{{apitype|CraftingOrderCustomerSearchResults}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|options}} || {{apitype|CraftingOrderCustomerOptionInfo[]}} || 
|-
| {{apiname|extraColumnType}} || {{apitype|Enum.AuctionHouseExtraColumn?}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ CraftingOrderCustomerOptionInfo
! Field !! Type !! Description
|-
| {{apiname|skillLineAbilityID}} || {{apitype|number}} || 
|-
| {{apiname|professionID}} || {{apitype|number}} || 
|-
| {{apiname|skillUpSkillLineID}} || {{apitype|number}} || 
|-
| {{apiname|spellID}} || {{apitype|number}} || 
|-
| {{apiname|itemID}} || {{apitype|number}} || 
|-
| {{apiname|itemName}} || {{apitype|string}} || 
|-
| {{apiname|primaryCategoryID}} || {{apitype|number}} || 
|-
| {{apiname|iLvlMin}} || {{apitype|number}} || <font color="green">10.0.7</font> - Renamed from <code>iLvl</code>
|-
| {{apiname|iLvlMax}} || {{apitype|number?}} || <font color="green">10.0.7</font>
|-
| {{apiname|canUse}} || {{apitype|boolean}} || <font color="green">10.0.5</font>
|-
| {{apiname|bindOnPickup}} || {{apitype|boolean}} || <font color="green">10.0.5</font>
|-
| {{apiname|qualityIlvlBonuses}} || {{apitype|number[]?}} || 
|-
| {{apiname|craftingQualityIDs}} || {{apitype|number[]?}} || 
|-
| {{apiname|quality}} || {{apitype|Enum.ItemQuality?}} || 
|-
| {{apiname|slots}} || {{apitype|number?}} || 
|-
| {{apiname|level}} || {{apitype|number?}} || 
|-
| {{apiname|skill}} || {{apitype|number?}} || 
|-
| {{apiname|secondaryCategoryID}} || {{apitype|number?}} || 
|-
| {{apiname|tertiaryCategoryID}} || {{apitype|number?}} || 
|-
| {{apiname|expansionID}} || {{apitype|number?}} || <font color="green">11.0.0</font>
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.AuctionHouseExtraColumn
! Value !! Field !! Description
|-
| 0 || {{apiname|None}} || 
|-
| 1 || {{apiname|Ilvl}} || 
|-
| 2 || {{apiname|Slots}} || 
|-
| 3 || {{apiname|Level}} || 
|-
| 4 || {{apiname|Skill}} || 
|}
```