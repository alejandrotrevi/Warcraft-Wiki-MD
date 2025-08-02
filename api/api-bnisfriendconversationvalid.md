# API BNIsFriendConversationValid

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether it is possible to converse with a specific battle.net friend.
 isConversationValid = BNIsFriendConversationValid(index)

==Arguments==
:;index:{{apitype|number}} - battle.net friend index to query, ascending from 1 to {{api|BNGetNumFriends}}().

==Returns==
:;isConversationValid:{{apitype|boolean}} - true if you can start a conversation with the specified battle.net friend, false otherwise.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}
```