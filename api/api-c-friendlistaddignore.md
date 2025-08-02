# API C FriendList.AddIgnore

**Contributor:** Cloudbells

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Adds a player to your ignore list.
 added = C_FriendList.AddIgnore(name)

==Arguments==
:;name:{{apitype|string}} - the name of the player you would like to ignore.

==Returns==
:;added:{{apitype|boolean}} - whether the player was succesfully added to your ignore list. This seems to ''only'' return false when trying to ignore someone who is already being ignored, otherwise true.

==Details==
* You can have a maximum of 50 people on your ignore list at the same time.
* The player being ignored does not need to be online for this to work.
* Calling this function when a player is already ignored will ignore (;D) the request.

==Patch changes==
* {{Patch 8.1.0|note=Moved into ''C_FriendList''. The former alias {{api|AddIgnore}} is deprecated and will be removed in the following expansion.}}
```