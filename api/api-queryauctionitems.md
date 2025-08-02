# API QueryAuctionItems

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Queries the server for information about current auctions, only when {{api|CanSendAuctionQuery}}() is true.
 QueryAuctionItems(text, minLevel, maxLevel, page, usable, rarity, getAll, exactMatch, filterData)

==Arguments==
:;text:{{apitype|string}} -  A part of the item's name, or an empty string; limited to 63 bytes.
:;minLevel:{{apitype|number?}} - Minimum usable level requirement for items
:;maxLevel:{{apitype|number?}} - Maximum usable level requirement for items
:;page:{{apitype|number}} -  What page in the auctionhouse this shows up. Note that pages start at 0.
:;usable:{{apitype|boolean}} - Restricts items to those usable by the current character.
:;rarity:{{apitype|Enum.ItemQuality?}} - Restricts the quality of the items found.
:;getAll:{{apitype|boolean}} - Download the entire auction house as one single page; see other details below.
:;exactMatch:{{apitype|boolean}} - Will only items whose whole name is the same as searchString be found.
:;filterData:{{apitype|table?}}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| classID || {{apitype|number}} || [[ItemType]]
|-
| subClassID || {{apitype|number?}} || Depends on the [[ItemType]]
|-
| inventoryType || {{apitype|Enum.InventoryType?}} ||
|}

==Details==
* Queries appear to be throttled at 0.3 seconds normally, or 15 minutes with ''getAll'' mode.  The return values from {{api|CanSendAuctionQuery}}() indicate when each mode is permitted.
* ''getAll'' mode might disconnect players with low bandwidth. Also see relevant details on client-to-server traffic in {{api|GetAuctionItemInfo}}()
* ''text'' longer than 63 bytes might disconnect the player.
* If any of the entered arguments is of the wrong type, the search assumes a nil value.
* No effect if the auction house window is not open.

:{{icon-exclamation}} In 4.0.1, ''getAll'' mode only fetches up to 42554 items.  This is usually adequate, but high-population realms might have more.

==Example==
Searches for rare items between levels 10 and 19:
 QueryAuctionItems("", 10, 19, 0, nil, nil, false, false, nil)

Searches for anything with the word "Nobles" in it, such as the Darkmoon card deck:
 /script QueryAuctionItems("Nobles", nil, nil, 0, false, nil, false, false, nil)

==Patch changes==
* {{Patch 8.3.0|note=Removed, replaced with {{api|C_AuctionHouse.SendBrowseQuery}}() and {{api|C_AuctionHouse.ReplicateItems}}().}}
* {{Patch 7.0.3|note=Replaced ''invType'', ''class'' and ''subclass'' with ''filterData''; shifting other arguments to earlier positions.<ref>{{ref FrameXML|Blizzard_AuctionUI/Blizzard_AuctionUI.lua|7.0.3|22267|410|2016-07-19}}</ref>}}
* {{Patch 2.3.0|note=Added ''getAll'' argument.}}

==References==
{{Reflist}}

{{apinavbox|AuctionHouse}}
```