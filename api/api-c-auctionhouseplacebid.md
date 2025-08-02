# API C AuctionHouse.PlaceBid

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}} {{restrictedapi|hwevent,noscript}}
Places a bid on a non-commodity item.
 C_AuctionHouse.PlaceBid(auctionID, bidAmount)

==Arguments==
:;auctionID:{{apitype|number}}
:;bidAmount:{{apitype|number}} - Amount in copper, only accepts gold and silently fails for non-zero copper counts.

==Example==
These examples require you to click a specific price listing from the available auctions first.
* Buys the currently selected auction.
<syntaxhighlight lang="lua">
function Example() -- /run Example()
	local buyFrame = AuctionHouseFrame.ItemBuyFrame
	C_AuctionHouse.PlaceBid(buyFrame.auctionID, buyFrame.BuyoutFrame.price)
end
</syntaxhighlight>

* Presses the "Buyout" button, in a macro suitable format which uses a secure template.
<syntaxhighlight lang="lua">
/run if not B then local f=CreateFrame("Button","B",nil,"SecureActionButtonTemplate")f:SetAttribute("type","click")f:SetAttribute("clickbutton",AuctionHouseFrame.ItemBuyFrame.BuyoutFrame.BuyoutButton)end
/click B LeftButton 1
/click StaticPopup1Button1
</syntaxhighlight>
[[File:API_C_AuctionHouse.PlaceBid.png]]

==Patch changes==
* {{Patch 9.1.5|note=Protected when called from a (macro) script.}}
* {{Patch 8.3.0|note=Added.}}

==See also==
* {{api|C_AuctionHouse.StartCommoditiesPurchase}}()
* https://www.curseforge.com/wow/addons/magic-button/ - Adds macros for keybinds to buy, post, and cancel on the auction house.

{{apinavbox|C_AuctionHouse}}
```