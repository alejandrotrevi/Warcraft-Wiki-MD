# API C FriendList.SetSelectedFriend

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Updates the current selected friend.

 C_FriendList.SetSelectedFriend(index)

==Arguments==
:;index:{{apitype|number}} - the index of the friend to be selected.

==Details==
* This function is necessary because indices can change in response to friend status updates.

==Patch changes==
* {{Patch 8.1.0|note=Moved to ''C_FriendList''. The former alias {{api|SetSelectedFriend}} is deprecated and will be removed in the following expansion.}}
```