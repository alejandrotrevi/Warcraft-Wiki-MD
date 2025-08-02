# API BNSendWhisper

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sends a whisper to Battle.net friends.
 BNSendWhisper(bnetAccountID, message)

==Arguments==
:;bnetAccountID:{{apitype|number}} - A unique numeric identifier for the friend during this session. You can get bnetAccountID from {{api|C_BattleNet.GetFriendAccountInfo}}()
:;message:{{apitype|string}} - Message text. Must be less than 4096 bytes.

The recipient will receive a [[CHAT_MSG_BN_WHISPER]] event, and the sender will also get a mirrored response from the server as [[CHAT_MSG_BN_WHISPER_INFORM]].
```