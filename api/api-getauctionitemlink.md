# API GetAuctionItemLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieves the [[itemLink]] of one item in the current retrieved list of items from the Auction House.

 itemLink = GetAuctionItemLink(type, index)

==Arguments==
:;type:{{apitype|string}} - One of the following:
:::;"list" : An item up for auction, the "Browse" tab in the dialog.
:::;"bidder" : An item the player has bid on, the "Bids" tab in the dialog.
:::;"owner" : An item the player has up for auction, the "Auctions" tab in the dialog.
:;index:{{apitype|number}} - The index of the item in the list to retrieve info from (normally 1-50, inclusive)

==Returns==
:;itemLink : [[itemLink]] - The itemLink for the specified item or
:: nil, if type and/or index is invalid.

{{apinavbox|AuctionHouse}}
```