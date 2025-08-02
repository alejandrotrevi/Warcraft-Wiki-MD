# API C AuctionHouse.SendSearchQuery

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}} {{restrictedapi|noscript|note=Otherwise it will brick the AH.}}
Queries an item in the auction house.
 C_AuctionHouse.SendSearchQuery(itemKey, sorts, separateOwnerItems [, minLevelFilter [, maxLevelFilter]])

==Arguments==
:;itemKey:{{apitype|ItemKey}}
{{:Struct ItemKey|nocaption=1}}
:;sorts:{{apitype|AuctionHouseSortType[]}}
{{:Struct AuctionHouseSortType|nocaption=1}}
:;separateOwnerItems:{{apitype|boolean}}
:;minLevelFilter:{{apitype|number?|default=0}}
:;maxLevelFilter:{{apitype|number?|default=0}}

==Details==
* Triggers the respective event for an item/commodity:
:: {{api|t=e|ITEM_SEARCH_RESULTS_UPDATED}} -> {{api|C_AuctionHouse.GetItemSearchResultInfo}}()
:: {{api|t=e|COMMODITY_SEARCH_RESULTS_UPDATED}} -> {{api|C_AuctionHouse.GetCommoditySearchResultInfo}}()
* Search queries are restricted to 100 calls per minute. These should not be used to query the entire auction house. See {{api|C_AuctionHouse.ReplicateItems}}()

==Example==
<onlyinclude>
Sends a [[API C_AuctionHouse.SendSearchQuery|search query]] for [[Storm Silver Ore]] when the button is pressed. Also prints results when manually browsing the AH.
<syntaxhighlight lang="lua">
local test_item = 5956 -- Blacksmith Hammer
local test_commodity = 152579 -- Storm Silver Ore

local btn = CreateFrame("Button", nil, UIParent, "UIPanelButtonTemplate")
btn:SetPoint("CENTER")
btn:SetSize(120, 40)
btn:SetText("Example")
btn:SetScript("OnClick", function(self, button)
	local itemKey = C_AuctionHouse.MakeItemKey(test_commodity)
	C_AuctionHouse.SendSearchQuery(itemKey, {}, false)
end)

local f = CreateFrame("Frame")

function f:ITEM_SEARCH_RESULTS_UPDATED(event, itemKey)
	for i = 1, C_AuctionHouse.GetNumItemSearchResults(itemKey) do
		local result = C_AuctionHouse.GetItemSearchResultInfo(itemKey, i)
		print(event, itemKey.itemID, i, result.auctionID, result.buyoutAmount)
	end
end

function f:COMMODITY_SEARCH_RESULTS_UPDATED(event, itemID)
	for i = 1, C_AuctionHouse.GetNumCommoditySearchResults(itemID) do
		local result = C_AuctionHouse.GetCommoditySearchResultInfo(itemID, i)
		print(event, itemID, i, result.quantity, result.auctionID, result.unitPrice)
	end
end

function f:OnEvent(event, ...)
	self[event](self, event, ...)
end

f:RegisterEvent("ITEM_SEARCH_RESULTS_UPDATED")
f:RegisterEvent("COMMODITY_SEARCH_RESULTS_UPDATED")
f:SetScript("OnEvent", f.OnEvent)
</syntaxhighlight></onlyinclude>

Addendum: for sorting it requires an array of {{apitype|AuctionHouseSortType}}. This sorts by price (ascending), and then level (descending).
<syntaxhighlight lang="lua">
local sorts = {
	{sortOrder = Enum.AuctionHouseSortOrder.Price, reverseSort = false},
	{sortOrder = Enum.AuctionHouseSortOrder.Level, reverseSort = true},
}

C_AuctionHouse.SendSearchQuery(itemKey, sorts, false)
</syntaxhighlight>

==Patch changes==
* {{Patch 9.1.0|note=Added <code>minLevelFilter, maxLevelFilter</code> arguments.}}
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```