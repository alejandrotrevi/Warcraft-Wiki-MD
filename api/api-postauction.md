# API PostAuction

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent,noscript}}
Posts the auction item from the Create Auction panel.
 PostAuction(minBid, buyoutPrice, runTime, stackSize, numStacks, warningAcknowledged)

==Arguments==
:;minBid:{{apitype|number}} - The minimum bid price for this auction in copper.
:;buyoutPrice:{{apitype|number}} - The buyout price for this auction in copper.
:;runTime:{{apitype|number}} - The duration for which the auction should be posted.
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Description
|-
| 1 || 2 hours (Medium)
|-
| 2 || 8 hours (Long)
|-
| 3 || 24 hours (Very Long)
|}
:;stackSize:{{apitype|number}} - The size of each stack to be posted.
:;numStacks:{{apitype|number}} - The number of stacks to post.
:;warningAcknowledged:{{apitype|boolean}} - Whether the warning popup about the major auction house maintenance was acknowledged. Passing <code>true</code> should be fine for users who don't care about possibly losing their deposit. Otherwise passing <code>false</code> will supposedly fail when there is an upcoming major maintance.

==Details==
* When the {{api|t=e|AUCTION_HOUSE_POST_WARNING}} event fires with the popup warning, requires <code>warningAcknowledged</code> to be true.
<syntaxhighlight lang="lua">
CONFIRM_AUCTION_POSTING_TEXT = "The auction house will undergo major updates during the scheduled weekly maintenance.|n|nIf your auction hasn't sold by then, your item will be returned early and you will lose your deposit."
</syntaxhighlight>

==Example==
[[File:API_PostAuction_01.jpg|thumb|right|Example auction post]]
Posts the item that is currently set to be auctioned
* bid price of 10 copper
* buyout price of 20 copper
* auction duration of 2 hours
* posts 2 auctions in stacks of 3
* posts the auction regardless of any scheduled major maintance warning
<syntaxhighlight lang="lua">
function Example() -- /run Example()
	PostAuction(10, 20, 1, 3, 2, true)
end
</syntaxhighlight>

==Patch changes==
* {{Patch 1.15.7|note=Added <code>warningAcknowledged</code> argument.}}
* {{Patch 1.13.2|note=Added. Replaces {{api|StartAuction}}()}}

{{apinavbox|AuctionHouse}}
```