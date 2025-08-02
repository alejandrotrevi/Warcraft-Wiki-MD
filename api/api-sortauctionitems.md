# API SortAuctionItems

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sorts the auction house display. Deprecated around Patch 2.0, see {{api|SortAuctionSetSort}}() which is almost functionally the same.
 SortAuctionItems(type, sort)

----
;''Arguments''
:(String type, String sort)

:;type:One of the following:
:::;"list" : An item up for auction, the "Browse" tab in the dialog.
:::;"bidder" : An item the player has bid on, the "Bids" tab in the dialog.
:::;"owner" : An item the player has up for auction, the "Auctions" tab in the dialog.

:;sort:One of the following:
:::;"quality" : The rarity of the item.
:::;"level" : The minimum required level (if any).  Only applies to "Browse" and "Bids" tabs.
:::;"status" : On the "Browse" tab, this is the "Seller" column.  On the "Bids" tab it is the "Bid Status" column.  On the "Auctions" tab it is the "High Bidder" column.
:::;"duration" : The amount of time left in the auction
:::;"bid" : An item the player has up for auction, the "Auctions" tab in the dialog.
:::;"name" : The name of the item.  Only applies to "Browse" and "Bids" tabs.  This is normally not shown as a separate sortable column (but is enabled with the AuctionSort adddon).
:::;"buyout" : An item the player has up for auction, the "Auctions" tab in the dialog.  This is normally not shown as a separate sortable column (but is enabled with the AuctionSort adddon).

----
;''Example''
 SortAuctionItems("list", "bid");

;''Result''

The results on the "Browse" tab are sorted by bid.

----
;''Details''

: There is no way to specifically set the direction of the sort.  It reverses the previous direction.  See also: [[API IsAuctionSortReversed|IsAuctionSortReversed(type, sort)]]

{{apinavbox|AuctionHouse}}
```