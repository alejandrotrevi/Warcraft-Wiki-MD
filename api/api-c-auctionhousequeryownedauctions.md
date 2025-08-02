# API C AuctionHouse.QueryOwnedAuctions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}} {{restrictedapi|noscript|note=Otherwise it will brick the AH.}}
Queries the auction house for the player's active auctions.
 C_AuctionHouse.QueryOwnedAuctions(sorts)

==Arguments==
:;sorts:{{apitype|AuctionHouseSortType[]}}
{{:Struct AuctionHouse.AuctionHouseSortType|nocaption=1}}

==Example==
Queries owned auctions, sorted by time remaining.
<syntaxhighlight lang="lua">
local btn = CreateFrame("Button", nil, UIParent, "UIPanelButtonTemplate")
btn:SetPoint("CENTER")
btn:SetSize(120, 40)
btn:SetText("Example")
btn:SetScript("OnClick", function(self, button)
	local sorts = {
		{sortOrder = Enum.AuctionHouseSortOrder.TimeRemaining, reverseSort = false},
	}
	C_AuctionHouse.QueryOwnedAuctions(sorts)
end)
</syntaxhighlight>

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

{{apinavbox|C_AuctionHouse}}
```