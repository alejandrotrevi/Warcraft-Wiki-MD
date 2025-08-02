# API SortAuctionSetSort

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the column by which the auction house sorts query results. This applies after the next search query or call to [[API SortAuctionApplySort|SortAuctionApplySort]](<span class="apiarg">type</span>)
 SortAuctionSetSort(type, column, reverse)

==Arguments==
:;type:{{apitype|string}} -  One of the following:
::*"list" - For items up for purchase, the "Browse" tab.
::*"bidder" - For items the player has bid on, the "Bids" tab.
::*"owner" - For items the player has posted, the "Auctions" tab.
:;column:{{apitype|string}} -  One of the following:
::*"quality" - The rarity of the item.
::*"level" - The minimum required level (if any). Only applies to "list" and "bidder" type views.
::*"status" - When the type is "list" this is the seller's name. For the "owner" type it is the high bidder's name.
::*"duration" - The amount of time left in the auction.
::*"bid" - The current bid amount for an auction.
::*"name" - The name of the item. This is a hidden column.
::*"buyout" - Buyout for the auction. This is a hidden column.
::*"unitprice" - Per-item (not per-stack) buyout price. This is a hidden and undocumented column.
:;reverse:{{apitype|boolean}} - Should the sort order be reversed.
{{apinavbox|AuctionHouse}}
```