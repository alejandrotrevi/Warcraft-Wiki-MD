# API GetNumAuctionItems

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieves the number of auction items of a certain type.
 batch,count = GetNumAuctionItems(list)

==Arguments==
:(string type)

:;type:One of the following:
:::;"list" : Items up for auction, the "Browse" tab in the dialog.
:::;"bidder" : Items the player has bid on, the "Bids" tab in the dialog.
:::;"owner" : Items the player has up for auction, the "Auctions" tab in the dialog.

==Returns==

:;batch:The size of the batch being viewed, 50 for a page view.
:;count:The total number of items in the query.

For a GetAll query, the batch and count are the same.

:{{icon-exclamation}}'''Bug''' seen in 4.0.1: If an AH has over 42554 items, ''batch'' will be retured as 42554, and ''count'' will be a seemingly random VERY HIGH number - ~1 billion has been seen.

==Example==
 numBatchAuctions, totalAuctions = GetNumAuctionItems("bidder");

{{apinavbox|AuctionHouse}}
```