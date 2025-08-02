# API C FriendList.IsIgnored

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether a character is being ignored by you.
 isIgnored = C_FriendList.IsIgnored(token)

==Arguments==
:;token:{{apitype|string}} - The [[UnitId]] or name of the character.

==Returns==
:;isIgnored:{{apitype|boolean}} - whether the character is ignored.

==Patch changes==
* {{Patch 8.1.0|note=Moved to ''C_FriendList''. The previous alias {{api|IsIgnored}} is deprecated and will be removed in the next expansion.}}
```