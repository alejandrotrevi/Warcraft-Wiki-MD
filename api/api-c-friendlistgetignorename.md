# API C FriendList.GetIgnoreName

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of a currently ignored player.

 name = C_FriendList.GetIgnoreName(index)

==Arguments==
:;index:{{apitype|number}} - index of the ignored player, up to {{api|C_FriendList.GetNumIgnores}} (max 50).

==Returns==
:;name:{{apitype|string?}} - name of the ignored player.

==Patch changes==
* {{Patch 8.1.0|note=Moved to ''C_FriendList''. The former alias {{api|GetIgnoreName}} is deprecated and will be removed in the following expansion.}}
```