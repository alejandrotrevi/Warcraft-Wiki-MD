# API C FriendList.GetSelectedFriend

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index of the currently selected friend.
 index = C_FriendList.GetSelectedFriend()

==Returns==
:;index:{{apitype|number?}} - The index of the friend which is currently selected on the friend list. Returns <code>nil</code> if you have no friends.

==Details==
* This function is necessary because indices can change in response to friend status updates.

==Patch changes==
* {{Patch 8.1.0|note=Moved to ''C_FriendList''. The former alias {{api|GetSelectedFriend}} is deprecated and will be removed in the following expansion.}}
```