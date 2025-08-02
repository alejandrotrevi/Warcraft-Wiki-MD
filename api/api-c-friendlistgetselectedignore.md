# API C FriendList.GetSelectedIgnore

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the currently selected index in the ignore listing.

 index = C_FriendList.GetSelectedIgnore()

==Returns==
:;index:{{apitype|number?}} - the index of the ignored player which is currently selected on the friend list. Returns <code>nil</code> if you have nobody ignored.

==Patch changes==
* {{Patch 8.1.0|note=Moved to ''C_FriendList''. The former alias {{api|GetSelectedIgnore}} is deprecated and will be removed in the following expansion.}}
```