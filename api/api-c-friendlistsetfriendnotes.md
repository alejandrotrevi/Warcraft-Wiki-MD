# API C FriendList.SetFriendNotes

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the note text for a friend.
 found = C_FriendList.SetFriendNotes(name, notes)

==Arguments==
:;name:{{apitype|string}} - name of friend in the friend list.
:;notes:{{apitype|string}} - the text that the friends note will be set to, up to 48 characters, anything longer will be truncated.

==Returns==
:;found:{{apitype|boolean}} - Whether the friend's note was successfully set.

==Patch changes==
* {{Patch 8.1.0|note=Moved to ''C_FriendList''. The former alias {{api|SetFriendNotes}} is deprecated and will be removed in the following expansion.}}
```