# API C BlackMarket.GetItemInfoByID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a [[Black Market]] auction.
 name, texture, quantity, itemType, usable, level, levelType, sellerName, minBid, minIncrement, currBid, youHaveHighBid, numBids, timeLeft, link, marketID, quality
   = C_BlackMarket.GetItemInfoByID(marketID)
   = C_BlackMarket.GetItemInfoByIndex(index)
   = C_BlackMarket.GetHotItem()

You can use <code>GetHotItem</code> to retrieve information about a "Hot Item!" auction picked by the server, <code>GetItemInfoByIndex</code> to iterate through all auctions, and <code>GetItemInfoByID</code> to retrieve information about specific auctions. These three functions have identical return values.

==Arguments==
===<font color="#4ec9b0">GetItemInfoByID</font>===
:;marketID:{{apitype|number}} - black market auction ID.
===<font color="#4ec9b0">GetItemInfoByIndex</font>===
:;index:{{apitype|number}} - black market auction index, ascending from 1 to {{api|C_BlackMarket.GetNumItems}}()

==Returns==
:;name:{{apitype|string}} - item name; nil if no such auction exists.
:;texture:{{apitype|string}} - icon texture path.
:;quantity:{{apitype|number}} - amount of the item included in the auction.
:;itemType:{{apitype|string}} - item type, e.g. "Quest", "Mail", or "Companion Pet"
:;usable:{{apitype|boolean}}
:;level:{{apitype|number}} - item level requirement.
:;levelType:{{apitype|string}} - e.g. "REQ_LEVEL_ABBR"
:;sellerName:{{apitype|string}} - localized name of the NPC "selling" the item.
:;minBid:{{apitype|number}} - minimum amount of copper you can bid for this item.
:;minIncrement:{{apitype|number}} - minimum amount of copper you must increase the current bid by.
:;currBid:{{apitype|number}} - the maximum current bid in copper.
:;youHaveHighBid:{{apitype|boolean}} - true if your bid on this item is currently the highest bid, false otherwise.
:;numBids:{{apitype|number}} - number of bids made on this item.
:;timeLeft:{{apitype|number}} - token indicating remaining auction duration, 0 for completed auctions, larger values indicate larger remaining durations. For a localized text version, use <code>_G["AUCTION_TIME_LEFT" .. timeLeft]</code>.
:;link:{{apitype|string}} - Chat link of the item being auctioned.
:;marketID:{{apitype|number}} - Black Market auction ID of this auction.
:;quality:{{apitype|number}}

==Details==
* These functions will only return information when the black market UI is open (according to the server, i.e. {{api|t=e|BLACK_MARKET_OPEN}} has fired, and {{api|t=e|BLACK_MARKET_CLOSE}} has not fired since).
* You may refresh available information by calling {{api|C_BlackMarket.RequestItems}}; {{api|t=e|BLACK_MARKET_ITEM_UPDATE}} fires to indicate that the return values of these functions may have changed.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

<!-- luals
---@param marketID number
---@return string name
---@return string texture
---@return number quantity
---@return string itemType
---@return boolean usable
---@return number level
---@return string levelType
---@return string sellerName
---@return number minBid
---@return number minIncrement
---@return number currBid
---@return boolean youHaveHighBid
---@return number numBids
---@return number timeLeft
---@return string link
---@return number marketID
---@return number quality
function C_BlackMarket.GetItemInfoByID(marketID) end

---[Documentation](https://warcraft.wiki.gg/wiki/API_C_BlackMarket.GetItemInfoByIndex)
---@param index number
---@return string name
---@return string texture
---@return number quantity
---@return string itemType
---@return boolean usable
---@return number level
---@return string levelType
---@return string sellerName
---@return number minBid
---@return number minIncrement
---@return number currBid
---@return boolean youHaveHighBid
---@return number numBids
---@return number timeLeft
---@return string link
---@return number marketID
---@return number quality
function C_BlackMarket.GetItemInfoByIndex(index) end

---[Documentation](https://warcraft.wiki.gg/wiki/API_C_BlackMarket.GetHotItem)
---@return string name
---@return string texture
---@return number quantity
---@return string itemType
---@return boolean usable
---@return number level
---@return string levelType
---@return string sellerName
---@return number minBid
---@return number minIncrement
---@return number currBid
---@return boolean youHaveHighBid
---@return number numBids
---@return number timeLeft
---@return string link
---@return number marketID
---@return number quality
function C_BlackMarket.GetHotItem() end
-->
```