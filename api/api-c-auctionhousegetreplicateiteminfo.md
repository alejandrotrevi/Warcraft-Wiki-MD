# API C AuctionHouse.GetReplicateItemInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns information about the specified auction.
 name, texture, count, qualityID, usable, level, levelType, minBid, minIncrement, buyoutPrice, bidAmount, highBidder, bidderFullName, owner, ownerFullName, saleStatus, itemID, hasAllInfo = C_AuctionHouse.GetReplicateItemInfo(index)

==Arguments==
:;index:{{apitype|number}} - index, ranging from 0 up to {{api|C_AuctionHouse.GetNumReplicateItems}}()-1

==Returns==
:;1. name:{{apitype|string?}}
:;2. texture:{{apitype|number?}}
:;3. count:{{apitype|number}}
:;4. qualityID:{{apitype|number}}
:;5. usable:{{apitype|boolean?}}
:;6. level:{{apitype|number}}
:;7. levelType:{{apitype|string?}}
:;8. minBid:{{apitype|number}}
:;9. minIncrement:{{apitype|number}}
:;10. buyoutPrice:{{apitype|number}}
:;11. bidAmount:{{apitype|number}}
:;12. highBidder:{{apitype|string?}}
:;13. bidderFullName:{{apitype|string?}}
:;14. owner:{{apitype|string?}} - Always returns nil, except for your own auctions.
:;15. ownerFullName:{{apitype|string?}} - Always returns nil
:;16. saleStatus:{{apitype|number}}
:;17. itemID:{{apitype|number}}
:;18. hasAllInfo:{{apitype|boolean?}}

==Example==
Before and after all info is available for an auction item. Only <code>count</code>, <code>minBid</code>, <code>buyoutPrice</code> and <code>itemID</code> are available immediately. (Pre-hotfix dump with <code>owner</code> and <code>ownerFullName</code>)
 /dump C_AuctionHouse.GetReplicateItemInfo(1)

<syntaxhighlight lang="lua">
"", nil, 4, -1, false, 2766221440, nil, 0, 0, 40000, 0, nil, nil, nil, nil, 0, 36901, false
"Goldclover", 134211, 4, 1, true, 1, "REQ_LEVEL_ABBR", 0, 0, 40000, 0, nil, nil, "Rialini", "Rialini-Ahn'Qiraj", 0, 36901, true
</syntaxhighlight>

{{:API_C_AuctionHouse.ReplicateItems}}

==Patch changes==
* {{Patch 9.0.2|note=Hotfixed <code>owner</code> and <code>ownerFullName</code> to always return nil (except for your own auctions) as that seemed to be the cause of disconnects.}}
* {{Patch 8.3.0|note=Added. Replaces {{api|GetAuctionItemInfo}}()<sup>[https://www.townlong-yak.com/framexml/8.3.0/Blizzard_Deprecated/Deprecated_8_3_0.lua#15]</sup>}}

==See also==
* {{api|C_AuctionHouse.ReplicateItems}}()
* {{api|t=e|REPLICATE_ITEM_LIST_UPDATE}}

{{apinavbox|C_AuctionHouse}}
```