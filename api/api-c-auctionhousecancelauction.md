# API C AuctionHouse.CancelAuction

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}} {{restrictedapi|hwevent,noscript}}
Cancels an auction.
 C_AuctionHouse.CancelAuction(ownedAuctionID)

==Arguments==
:;ownedAuctionID:{{apitype|number}}

==Example==
* Cancels the currently selected auction.
<syntaxhighlight lang="lua">
function Example() -- /run Example()
	C_AuctionHouse.CancelAuction(AuctionHouseFrame.AuctionsFrame.selectedAuctionID)
end
</syntaxhighlight>

* Presses the "Cancel Auction" button, in a macro suitable format which uses a secure template.
<syntaxhighlight lang="lua">
/run if not CA then local f=CreateFrame("Button","CA",nil,"SecureActionButtonTemplate")f:SetAttribute("type","click")f:SetAttribute("clickbutton",AuctionHouseFrame.AuctionsFrame.CancelAuctionButton)end
/click CA LeftButton 1
/click StaticPopup1Button1
</syntaxhighlight>

==Patch changes==
* {{Patch 9.1.5|note=Protected when called from a (macro) script.}}
* {{Patch 8.3.0|note=Added.}}

==See also==
* https://www.curseforge.com/wow/addons/magic-button/ - Adds macros for keybinds to buy, post, and cancel on the auction house.

{{apinavbox|C_AuctionHouse}}
```