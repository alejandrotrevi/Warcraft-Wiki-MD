# API BNGetFriendInviteInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a Battle.net friend invite.
 inviteID, accountName, isBattleTag, message, sentTime = BNGetFriendInviteInfo(inviteIndex)

==Arguments==
:;inviteIndex:{{apitype|number}} - Ranging from 1 to {{api|BNGetNumFriendInvites}}()

==Returns==
:;inviteID:{{apitype|number}} - Also known as the presence id.
:;accountName:{{apitype|number}} - [[UI_escape_sequences#Protected_strings|Protected string]] for the friend account name, e.g. "|Kq4|k".
:;isBattleTag:{{apitype|boolean}}
:;message:{{apitype|string?}} - Appears to be always nil now.
:;sentTime:{{apitype|number}} - The unix time when the invite was sent/received.

==Patch changes==
* {{Patch 3.3.5|note=Added.}}
```