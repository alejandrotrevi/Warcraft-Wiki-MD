# API BNSendGameData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sends a hidden addon message to a Battle.net friend.
 BNSendGameData(gameAccountID, prefix, text)

==Arguments==
:;gameAccountID:{{apitype|number}} - The game account ID of the friend during this session.
:;prefix:{{apitype|string}} - An addon messaging prefix previously registered with {{api|C_ChatInfo.RegisterAddonMessagePrefix}}.
:;text:{{apitype|string}} - The data to be sent. Limited to 4078 bytes or less.

==Details==
* Triggers the {{api|t=e|BN_CHAT_MSG_ADDON}} event on receipt of a message.
* Delivery of Battle.net messages must '''not''' be assumed be in the same order that they are sent. Out-of-order delivery can be observed somewhat infrequently if many messages are sent to another player.

==Patch changes==
* {{Patch 5.4.7|note=Added.}}

==See also==
*{{api|BNSendWhisper}}(presenceID, message)
*[[BN_CHAT_MSG_ADDON]]

==References==
* http://us.battle.net/wow/en/forum/topic/11437004031
```