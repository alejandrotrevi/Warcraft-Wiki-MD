# API GetAuctionItemInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieves info about one item in the current retrieved list of items from the Auction House.
 name, texture, count, quality, canUse, level, levelColHeader, minBid, minIncrement, buyoutPrice, bidAmount, highBidder, bidderFullName, owner, ownerFullName, saleStatus, itemId, hasAllInfo = GetAuctionItemInfo(type, index)

==Arguments==
:;type:{{apitype|string}} -  One of the following:
::*"list" - An item up for auction, the "Browse" tab in the dialog.
::*"bidder" - An item the player has bid on, the "Bids" tab in the dialog.
::*"owner" - An item the player has up for auction, the "Auctions" tab in the dialog.
:;index:{{apitype|number}} - The index of the item in the list to retrieve info from (normally 1-50, inclusive)
==Returns==
:;1. name:{{apitype|string}} - the name of the item
:;2. texture:{{apitype|number}} - the [[fileID]] of the texture of the item
:;3. count:{{apitype|number}} - the number of items in the auction item, zero if item is "sold" in the "owner" auctions
:;4. quality:{{apitype|Enum.ItemQuality}}
:;5. canUse:{{apitype|boolean}} - true if the user can use the item, false if not
:;6. level:{{apitype|number}} - the level required to use the item,
:;7. levelColHeader:{{apitype|string}} - The preceding ''level'' return value changes depending on the value of levelColHeader:
:* "REQ_LEVEL_ABBR" - level represents the required character level
:* "SKILL_ABBR" - level represents the required skill level (for recipes)
:* "ITEM_LEVEL_ABBR" - level represents the item level
:* "SLOT_ABBR" - level represents the number of slots (for containers)
:;8. minBid:{{apitype|number}} - the starting bid price
:;9. minIncrement:{{apitype|number}} - the minimum amount of item at which to put the next bid
:;10. buyoutPrice:{{apitype|number}} - zero if no buy out, otherwise it contains the buyout price of the auction item
:;11. bidAmount:{{apitype|number}} - the current highest bid, zero if no one has bid yet
:;12. highBidder:{{apitype|string?}} - returns name of highest bidder, nil otherwise
:;13. bidderFullName:{{apitype|string?}} - returns bidders full name if from virtual realm, nil otherwise
:;14. owner:{{apitype|string}} - the player that is selling the item
:;15. ownerFullName:{{apitype|string?}} - returns owners full name if from virtual realm, nil otherwise
:;16. saleStatus:{{apitype|number}} - 1 for sold 0 for unsold
:;17. itemId:{{apitype|number}} - item id
:;18. hasAllInfo:{{apitype|boolean}} - was everything returned

==Example==
<syntaxhighlight lang="lua">
-- Retrieves info about the first item in the list of your currently auctioned items.
local name, texture, count, quality, canUse, level, levelColHeader, minBid, minIncrement, buyoutPrice, bidAmount, 
    highBidder, bidderFullName, owner, ownerFullName, saleStatus, itemId, hasAllInfo =  GetAuctionItemInfo("owner", 1);
</syntaxhighlight>

==Details==

===Auctions being returned as nil===

As of 4.0.1, auctions will be returned as "nil" for items not yet in the client's itemcache. New items resolve at a rate of 30 unique [[ItemString|itemid]]s every 30 seconds. (Note that "of the Xxx" items share the same itemid)

Blizzard's standard auction house view overcomes this problem by reacting to AUCTION_ITEM_LIST_UPDATE and re-querying the items.

===The "owner" field and playername resolving===
Note that the "owner" field can be ''nil''. This happens because the auction listing internally contains player GUIDs rather than names, and the WoW client does not query the server for names until GetAuctionItemInfo() is actually called for the item, and the result takes one [[RTT]] to arrive. The GUID->name mapping is then stored in a name resolution cache, which gets cleared upon logout (not UI reload).

Blizzard's standard auction house view overcomes this problem by reacting to AUCTION_ITEM_LIST_UPDATE and re-querying the items.

However, this event-driven approach does not really work for e.g. scanner engines. There, the correct solution is to re-query items with nil owners for a short time (a low number of seconds). There IS a possibility that it NEVER returns something - this happens when someone puts something up for auction and then deletes his character. 


Note that the playername resolver will only resolve a certain number of sellers every 30 seconds. When this limit is exceeded, it will appear as if responses arrive in a batches every 30 seconds.

==Patch changes==
* {{Patch 7.3.0|note=Second return value (the texture or icon) changed from string to [[fileID]].}}
* {{Patch 5.4.0|note=Two new returns (bidderFullName at #13 and ownerFullName at #15) have been added.}}
* {{Patch 4.3.0|note=Added seventh return value, ''levelColHeader'', to specify the meaning of ''level''.{{fact}}}}

{{apinavbox|AuctionHouse}}
```