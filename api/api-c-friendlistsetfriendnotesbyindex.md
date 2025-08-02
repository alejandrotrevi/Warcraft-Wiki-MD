# API C FriendList.SetFriendNotesByIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the note text for a friend.
 C_FriendList.SetFriendNotesByIndex(index, notes)

==Arguments==
:;index:{{apitype|number}} - index of the friend, up to {{api|C_FriendList.GetNumFriends}} (max 100). Note that status changes can re-order the friend list, indices are not guaranteed to remain stable across events.
:;notes:{{apitype|string}} - the text that the friends note will be set to, up to 48 characters, anything longer will be truncated.

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```