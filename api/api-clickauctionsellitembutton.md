# API ClickAuctionSellItemButton

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
ClickAuctionSellItemButton(frame,button,boolean) - Puts the currently 'picked up' item into the 'create auction' slot. 

In the Auction house, under 'auctions', 'create auction', there is an 'auction item' slot. This
function lets you 'drop' your currently 'picked up' item into it. AFAIK It works as long as the 
'auction' window is up (the one you get by clicking on the auctioneer).


********************
Changes in 4.0
Frame: Unknown
Button: "Leftbutton","rightbutton",3,4,5  --the various mouse buttons that send the input
boolean: is the mouse button held down or not.


See Also:
*[[API_PickupContainerItem]]
*[[API_StartAuction]]
*[[World_of_Warcraft_API#Inventory_Functions]]
*[[World_of_Warcraft_API#Auction_Functions]]

{{apinavbox|AuctionHouse}}
```