# API C FriendList.AddFriend

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|noscript}}
Adds a friend to your friend list.
 C_FriendList.AddFriend(name [, notes])

==Arguments==
:;name:{{apitype|string}} - The name of the player you would like to add.
:;notes:{{apitype|string?}} - The note that will show in your friend list.

==Details==
* You can have a maximum of 100 people on your friends list at the same time.
* The player being added does not need to be online for this to work.

==Patch changes==
* {{Patch 9.1.5|note=Protected when called from a (macro) script.}}
* {{Patch 8.1.0|note=Moved to <code>C_FriendList.AddFriend()</code><sup>[https://www.townlong-yak.com/framexml/29701/Blizzard_Deprecated/Deprecated_8_1_0.lua#107]</sup>}}
* {{Patch 2.4.0|note=Added <code>notes</code> argument.<sup>[https://www.townlong-yak.com/framexml/2.4.0/ChatFrame.lua/diff#1560]</sup>}}
* {{Patch 1.0.0|note=Added as <code>AddFriend()</code>}}
```