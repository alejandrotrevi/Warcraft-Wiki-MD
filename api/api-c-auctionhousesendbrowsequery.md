# API C AuctionHouse.SendBrowseQuery

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}} {{restrictedapi|noscript|note=Otherwise it will brick the AH.}}
Queries the auction house using search parameters.
 C_AuctionHouse.SendBrowseQuery(query)

==Arguments==
:;query:{{apitype|AuctionHouseBrowseQuery}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| searchString || {{apitype|string}} || Case insensitive
|-
| sorts || {{apitype|AuctionHouseSortType[]}} || This appears to expect at least a certain combination of sort types, e.g. price and name.
|-
| minLevel || {{apitype|number?}} || 
|-
| maxLevel || {{apitype|number?}} || 
|-
| filters || {{apitype|Enum.AuctionHouseFilter[]?}} || Requires at least one filter in order to show something.
|-
| itemClassFilters || {{apitype|AuctionHouseItemClassFilter[]?}} || 
|}

{{:Struct_AuctionHouse.AuctionHouseSortType}}

{{:Enum_AuctionHouse.AuctionHouseFilter}}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ AuctionHouseItemClassFilter
! Field !! Type !! Description
|-
| classID || {{apitype|number}} || [[ItemType]]
|-
| subClassID || {{apitype|number?}} || 
|-
| inventoryType || {{apitype|Enum.InventoryType?}} || 
|}

==Example==
Queries auctions, sorted by price and then name. Shows only items from Poor to Epic quality.
<syntaxhighlight lang="lua">
local btn = CreateFrame("Button", nil, UIParent, "UIPanelButtonTemplate")
btn:SetPoint("CENTER")
btn:SetSize(120, 40)
btn:SetText("Example")
btn:SetScript("OnClick", function(self, button)
	local query = {
		searchString = "",
		sorts = {
			{sortOrder = Enum.AuctionHouseSortOrder.Price, reverseSort = false},
			{sortOrder = Enum.AuctionHouseSortOrder.Name, reverseSort = false},
		},
		filters = {
			Enum.AuctionHouseFilter.PoorQuality,
			Enum.AuctionHouseFilter.CommonQuality,
			Enum.AuctionHouseFilter.UncommonQuality,
			Enum.AuctionHouseFilter.RareQuality,
			Enum.AuctionHouseFilter.EpicQuality,
		},
	}
	C_AuctionHouse.SendBrowseQuery(query)
end)
</syntaxhighlight>

==Patch changes==
* {{Patch 8.3.0|note=Added, replacing {{api|QueryAuctionItems}}().}}

==See also==
* {{api|C_AuctionHouse.SendSearchQuery}}() - Query a specific ItemID.
* {{api|C_AuctionHouse.ReplicateItems}}() - Download the entire auction house.

{{apinavbox|C_AuctionHouse}}
```