# API C FriendList.RemoveFriend

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Removes a friend from the friends list.
 removed = C_FriendList.RemoveFriend(name)

==Arguments==
:;name:{{apitype|string}} - the name of the friend to remove.

==Returns==
:;removed:{{apitype|boolean}} - whether the friend was successfully removed.

==Patch changes==
* {{Patch 8.1.0|note=Moved to ''C_FriendList''. The previous alias {{api|RemoveFriend}} is deprecated and will be removed in the next expansion.}}
```