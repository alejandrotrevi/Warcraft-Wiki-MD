# API SetSelectedAuctionItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Selects a specific item in the auction house

 SetSelectedAuctionItem(type, index)

----
;''Arguments''
:(String type, Number index)

:;type:One of the following:
:::;"list" : An item up for auction, the "Browse" tab in the dialog.
:::;"bidder" : An item the player has bid on, the "Bids" tab in the dialog.
:::;"owner" : An item the player has up for auction, the "Auctions" tab in the dialog.

:;index:The index of the item in the list to retrieve info from (normally 1-50, inclusive)

{{apinavbox|AuctionHouse}}
```