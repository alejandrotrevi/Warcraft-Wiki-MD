# API PlaceAuctionBid

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Place a bid on the selected auction item.

 PlaceAuctionBid(type, index, bid)

----

;''Arguments''
:(string type)

:;type:One of the following:
:::;"list" : Items up for auction, the "Browse" tab in the dialog.
:::;"bidder" : Items the player has bid on, the "Bids" tab in the dialog.
:::;"owner" : Items the player has up for auction, the "Auctions" tab in the dialog.

:;index:The index of the item in the list to bid on (normally 1-50, inclusive)

:;bid:The amount of money to bid in copper.

----

It is important to know that this function can only be successfully called after a hardware event, e.g. mouse click on a prompt since patch 2.0.

{{apinavbox|AuctionHouse}}
```