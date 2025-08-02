# API GetAuctionItemTimeLeft

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieves the time left for a item in the Auction House.
 timeleft = GetAuctionItemTimeLeft(type, index)

----
;''Arguments''
:(String type, Number index)

:;type:{{apitype|string}} - One of the following:
:::;"list" : An item up for auction, the "Browse" tab in the dialog.
:::;"bidder" : An item the player has bid on, the "Bids" tab in the dialog.
:::;"owner" : An item the player has up for auction, the "Auctions" tab in the dialog.

:;index:{{apitype|number}} - The index of the item in the list to retrieve info from (normally 1-50, inclusive)

----
;''Returns''

:;timeleft:{{apitype|number}} - number between 1 and 4
:::;1 : short (less than 30 minutes)
:::;2 : medium (30 minutes - 2 hours)
:::;3 : long (2 - 12 hours)
:::;4 : very long (more than 12 hours)

----
;''Example''
 timeleft = GetAuctionItemTimeLeft("owner", offset + i);

;''Result''

Returns the time that the item will stay in the auction house. Affects nothing other than the return values.

----
;''Description''

: Retrieves the time left for an item in the current list of auction items.

{{apinavbox|AuctionHouse}}
```