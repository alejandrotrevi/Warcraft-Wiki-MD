# API C AuctionHouse.StartCommoditiesPurchase

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}} {{restrictedapi|hwevent,noscript}}
Starts a commodity item purchase.
 C_AuctionHouse.StartCommoditiesPurchase(itemID, quantity)

==Arguments==
:;itemID:{{apitype|number}}
:;quantity:{{apitype|number}}

==Details==
* The purchase is finalized with {{api|C_AuctionHouse.ConfirmCommoditiesPurchase}}()

==Example==
<onlyinclude>* Buys 3x [https://www.wowhead.com/item=2592/wool-cloth Wool Cloth] and uses a delay to wait for the auction house to process.
<syntaxhighlight lang="lua">
function Example() -- /run Example()
	C_AuctionHouse.StartCommoditiesPurchase(2592, 3)
	C_Timer.After(.5, function() C_AuctionHouse.ConfirmCommoditiesPurchase(2592, 3) end)
end
</syntaxhighlight>

* Waits for {{api|t=e|AUCTION_HOUSE_THROTTLED_SYSTEM_READY}} instead of using a delay. Note that <code>C_AuctionHouse.StartCommoditiesPurchase</code> requires a hardware event.
<syntaxhighlight lang="lua">
local item = {}

function TestPurchaseCommodity(itemID, quantity)
	C_AuctionHouse.StartCommoditiesPurchase(itemID, quantity)
	item.itemID = itemID
	item.quantity = quantity
end

local function OnEvent(self, event)
	if next(item) then
		C_AuctionHouse.ConfirmCommoditiesPurchase(item.itemID, item.quantity)
		wipe(item)
	end
end

local f = CreateFrame("Frame")
f:RegisterEvent("AUCTION_HOUSE_THROTTLED_SYSTEM_READY")
f:SetScript("OnEvent", OnEvent)

-- /run TestPurchaseCommodity(2592, 2)
</syntaxhighlight>

* Presses the "Buy" button, in a macro suitable format which uses a secure template. ''<font color="#4ec9b0">Split into two parts since it doesn't fit within <255 chars.</font>''
1. Initializes the secure template.
<syntaxhighlight lang="lua">
/run if not AHBuyC then local f=CreateFrame("Button","AHBuyC",nil,"SecureActionButtonTemplate")f:SetAttribute("type","click")f:SetAttribute("clickbutton",AuctionHouseFrame.CommoditiesBuyFrame.BuyDisplay.BuyButton)end
</syntaxhighlight>
2. Buys the commodity items.
<syntaxhighlight lang="lua">
/click AHBuyC LeftButton 1
/run C_Timer.After(1, function() AuctionHouseFrame.BuyDialog.BuyNowButton:Click() end)
</syntaxhighlight></onlyinclude>

==Patch changes==
* {{Patch 9.1.5|note=Protected when called from a (macro) script.}}
* {{Patch 8.3.0|note=Added.}}

==See also==
* https://www.curseforge.com/wow/addons/magic-button/ - Adds macros for keybinds to buy, post, and cancel on the auction house.

{{apinavbox|C_AuctionHouse}}
```