# API CanSendAuctionQuery

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Determine if a new auction house query can be sent (via [[API QueryAuctionItems|QueryAuctionItems]]())
 canQuery,canQueryAll = CanSendAuctionQuery()

==Returns==
:;canQuery:{{apitype|boolean}} - True if a normal auction house query can be made
:;canQueryAll:{{apitype|boolean}} - True if a full ("getall") auction house query can be made (added in 2.3)

==Details==
* There is always a short delay (usually less than a second) after each query before another query can take place.
* Full ("getall") queries are only allowed once every ~15 minutes.

{{apinavbox|AuctionHouse}}
```