# API BeginTrade

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Accepts an offer to start trading with another player.
 BeginTrade()

==Details==
* {{api|t=e|TRADE_REQUEST}} notifies you of a pending request to trade; the name of the initiating player is provided as the first argument in the event.
* You may accept a trade request using this function, or reject it using {{api|CancelTrade}}.
* {{api|t=e|TRADE_REQUEST_CANCEL}} fires if the offering player rescinds the invitation to trade (or moves out of range).
```