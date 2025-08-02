# API GetAuctionItemBattlePetInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieves info about one Battle Pet in the current retrieved list of Battle Pets from the Auction House.
 creatureID, displayID = GetAuctionItemBattlePetInfo(type, index)

==Arguments==
:;type:{{apitype|string}} - One of the following:
::*"list" - An item up for auction, the "Browse" tab in the dialog.
::*"bidder" - An item the player has bid on, the "Bids" tab in the dialog.
::*"owner" - An item the player has up for auction, the "Auctions" tab in the dialog.
:;index:{{apitype|number}} - The index of the item in the list to retrieve info from (normally 1-50, inclusive).

==Returns==
:;creatureID:{{apitype|number}} - An indexing value Blizzard uses to number NPCs.
:;displayID:{{apitype|number}} - An indexing value Blizzard uses to number model/skin combinations.

==Details==
The displayID return appears to always be 0, possibly because the function is only used by Blizzard in conjunction with {{api|DressUpBattlePet}}.

==Patch changes==
* {{Patch 8.3.0|note=Replaced with {{api|C_AuctionHouse.GetReplicateItemBattlePetInfo}}}}
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|DressUpBattlePet}}
* {{api|GetAuctionItemInfo}}

{{apinavbox|AuctionHouse}}
```