# API C AuctionHouse.PostCommodity

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}} {{restrictedapi|hwevent,noscript}}
Posts a commodity item on the auction house.
 needsConfirmation = C_AuctionHouse.PostCommodity(item, duration, quantity, unitPrice)

==Arguments==
:;item:{{apitype|ItemLocationMixin}}
:;duration:{{apitype|number}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Description
|-
| 1 || 12 Hours
|-
| 2 || 24 Hours
|-
| 3 || 48 Hours
|}
:;quantity:{{apitype|number}}
:;unitPrice:{{apitype|number}} - Amount in copper, only accepts gold and silver and silently fails for non-zero copper counts.

==Returns==
:;needsConfirmation:<span class="apitype">boolean</span>

==Example==
Auctions 14 units of the commodity item in the topleft corner of your default backpack, for 48 hours with a 27 silver price per unit.
<syntaxhighlight lang="lua">
function Example() -- /run Example()
	C_AuctionHouse.PostCommodity(ItemLocation:CreateFromBagAndSlot(0, 1), 3, 14, 2700)
end
</syntaxhighlight>

* Presses the "Create Auction" button, in a macro suitable format which uses a secure template.
<syntaxhighlight lang="lua">
/run if not AHPostC then local f=CreateFrame("Button","AHPostC",nil,"SecureActionButtonTemplate")f:SetAttribute("type","click")f:SetAttribute("clickbutton",AuctionHouseFrame.CommoditiesSellFrame.PostButton)end
/click AHPostC LeftButton 1
</syntaxhighlight>

* This would brick the Auction House.
 /run AuctionHouseFrame.CommoditiesSellFrame.PostButton:Click()

==Patch changes==
* {{Patch 9.2.5|note=Added <code>needsConfirmation</code> return.}}
* {{Patch 9.1.5|note=Protected when called from a (macro) script.}}
* {{Patch 8.3.0|note=Added. Requires a hardware event.}}

==See also==
* {{api|t=a|C_AuctionHouse.PostItem}}()
* https://www.curseforge.com/wow/addons/magic-button/ - Adds macros for keybinds to buy, post, and cancel on the auction house.

{{apinavbox|C_AuctionHouse}}
```