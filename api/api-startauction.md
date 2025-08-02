# API StartAuction

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
{{Ambox
| image = [[Image:Icon-boilerplate-48x48.png]]
| border = red
| type = This API is deprecated and no longer works.<sup>[https://github.com/Gethe/wow-ui-source/blob/d230032c711fb01aef144820302f68b4786c3ab6/Interface_TBC/FrameXML/StaticPopup.lua#L4560]</sup>
| info = 
* It was replaced by {{api|PostAuction}}()
}}
<!--desc-->Starts the auction you have created in the Create Auction panel.
 StartAuction(minBid, buyoutPrice, runTime, stackSize, numStacks)

The item is that which has been put into the AuctionSellItemButton. That's the slot in the 'create auction' panel. 

The minBid and buyoutPrice are in copper. However I cant figure out how to go below 1 silver. So putting in
'50' or '10' or '1' will always make the auction do '1 silver'. But '102' will make it do '1 silver 2 copper'.  

runTime may be one of the following:  1, 2, 3  for 12, 24, and 48 hours.

Examples:

 StartAuction(1,1,1)         - Start at 1 silver, buyout 1 silver, time 12 hours
 StartAuction(1,10,1)        - Start at 1 silver, buyout 1 silver, time 12 hours
 StartAuction(1,100,1)       - Start at 1 silver, buyout 1 silver, time 12 hours
 StartAuction(1,1000,1)      - Start at 1 silver, buyout 10 silver, time 12 hours
 StartAuction(1,10000,2)     - Start at 1 silver, buyout 1 gold, time 24 hours
 StartAuction(101,150,3)     - Start at 1 silver 1 copper, buyout at 1 silver 50 copper, time 48 hours

Play with it yourself: 

*Go to auction house
*Right click on auctioneer
*Click on the 'auction' tab
*Drag an item to the slot in the 'Create Auction' panel
*Type the following into chat window:

 /script StartAuction(1,150,1)

*This should create an auction starting at 1 silver, buyout at 1 silver 50 copper, with auction time of 12 hours.
*It should say 'Auction Created' in the chat window. 
*Now if you go to browse the auctions, your items should show up.

==Details==
* As of Patch 4.0, StartAuction() requires a hardware event.  This change does not show up in any patch documentation.

{{apinavbox|AuctionHouse}}
```