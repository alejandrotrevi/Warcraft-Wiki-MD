# API C FriendList.DelIgnore

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Removes a player from your ignore list.
 removed = C_FriendList.DelIgnore(name)

==arguments==
:;name:{{apitype|string}} - the name of the player you would like to remove from your ignore list.

==Returns==
:;removed:{{apitype|boolean}} - whether the player was succesfully removed from your ignore list.

==Patch changes==
* {{Patch 8.1.0|note=Moved to ''C_FriendList''. The former alias {{api|DelIgnore}} is deprecated and will be removed in the following expansion.}}
```