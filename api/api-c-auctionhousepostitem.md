# API C AuctionHouse.PostItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}} {{restrictedapi|hwevent,noscript}}
Posts an item on the auction house.
 needsConfirmation = C_AuctionHouse.PostItem(item, duration, quantity [, bid [, buyout]])

==Arguments==
:;item:{{apitype|ItemLocationMixin}}
:;duration:{{apitype|number}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Description
|-
| 1 || 12 hours
|-
| 2 || 24 hours
|-
| 3 || 48 hours
|}
:;quantity:{{apitype|number}} - The <code>quantity</code> for items can be bigger than 1, it will not be limited to the given ItemLocation and continue auctioning items from the other slots in your backpack.
:;bid:{{apitype|number?}} - Either <code>bid</code> or <code>buyout</code> has to be supplied, or both. Amount in copper, only accepts gold and silver and silently fails for non-zero copper counts.
:;buyout:{{apitype|number?}}

==Returns==
:;needsConfirmation:<span class="apitype">boolean</span>

==Example==
* Auctions the non-commodity item in the topleft corner of your default backpack, for 48 hours with a 42 silver buyout.
<syntaxhighlight lang="lua">
function Example() -- /run Example()
	C_AuctionHouse.PostItem(ItemLocation:CreateFromBagAndSlot(0, 1), 3, 1, nil, 4200)
end
</syntaxhighlight>

* Presses the "Create Auction" button, in a macro suitable format which uses a secure template.
<syntaxhighlight lang="lua">
/run if not AHPost then local f=CreateFrame("Button","AHPost",nil,"SecureActionButtonTemplate")f:SetAttribute("type","click")f:SetAttribute("clickbutton",AuctionHouseFrame.ItemSellFrame.PostButton)end
/click AHPost LeftButton 1
</syntaxhighlight>

* This would brick the Auction House.
 /run AuctionHouseFrame.ItemSellFrame.PostButton:Click()

==Patch changes==
* {{Patch 9.2.5|note=Added <code>needsConfirmation</code> return.}}
* {{Patch 9.1.5|note=Protected when called from a (macro) script.}}
* {{Patch 8.3.0|note=Added.}}

==See also==
* {{api|t=a|C_AuctionHouse.PostCommodity}}()
* https://www.curseforge.com/wow/addons/magic-button/ - Adds macros for keybinds to buy, post, and cancel on the auction house.

{{apinavbox|C_AuctionHouse}}
```