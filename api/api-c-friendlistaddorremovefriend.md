# API C FriendList.AddOrRemoveFriend

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Adds or removes a player to or from the friends list.
 C_FriendList.AddOrRemoveFriend(name, notes)

==Arguments==
:;name:{{apitype|string}} - The name of the player to add or remove.
:;notes:{{apitype|string}} - (Required) The note in the friends frame.

==Details==
* If the player is already on your friends list, the player will be removed regardless of whether you pass <code>notes</code> as the second argument.
```