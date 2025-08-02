# API C FriendList.GetFriendInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_FriendList|system=FriendList}}
Retrieves information about a person on your friends list.
 info = C_FriendList.GetFriendInfo(name)
      = C_FriendList.GetFriendInfoByIndex(index)

==Arguments==
===<font color="#4ec9b0">GetFriendInfo</font>===
:;name:{{apitype|string}} - name of friend in the friend list.

===<font color="#4ec9b0">GetFriendInfoByIndex</font>===
:;index:{{apitype|number}} - index of the friend, up to {{api|C_FriendList.GetNumFriends}}() limited to max 100.

==Returns==
:;info:{{apitype|FriendInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|connected}} || {{apitype|boolean}} || If the friend is online
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|className}} || {{apitype|string?}} || Friend's class, or "Unknown" (if offline)
|-
| {{apiname|area}} || {{apitype|string?}} || Current location, or "Unknown" (if offline)
|-
| {{apiname|notes}} || {{apitype|string?}} || 
|-
| {{apiname|guid}} || {{apitype|WOWGUID}} || [[GUID]], example: "Player-1096-085DE703"
|-
| {{apiname|level}} || {{apitype|number}} || Friend's level, or 0 (if offline)
|-
| {{apiname|dnd}} || {{apitype|boolean}} || If the friend's current status flag is DND
|-
| {{apiname|afk}} || {{apitype|boolean}} || If the friend's current status flag is AFK
|-
| {{apiname|rafLinkType}} || {{apitype|Enum.RafLinkType}} || 
|}

==Details==
* Friend information isn't necessarily automatically kept up to date. You can use {{api|C_FriendList.ShowFriends}}() to request an update from the server.

==Example==
<syntaxhighlight lang="lua">
local f = C_FriendList.GetFriendInfoByIndex(1)
print(format("Your friend %s (level %d %s) is in %s", f.name, f.level, f.className, f.area))
-- Your friend Aërto (level 74 Warrior) is in Sholazar Basin
</syntaxhighlight>

==Patch changes==
* {{Patch 11.0.5|note=Removed <code>mobile</code> field.}}
* {{Patch 8.2.5|note=Added <code>rafLinkType</code> field.}}
* {{Patch 8.2.0|note=Added <code>mobile</code> field.}}
* {{Patch 8.1.0|note=Moved to <code>C_FriendList.GetFriendInfo()</code><sup>[https://www.townlong-yak.com/framexml/8.1.5/Blizzard_Deprecated/Deprecated_8_1_0.lua#70]</sup>}}
* {{Patch 2.4.0|note=Added <code>note</code> return.<sup>[https://www.townlong-yak.com/framexml/2.4.0/FriendsFrame.lua/diff#201]</sup>}}
* {{Patch 1.0.0|note=Added as <code>GetFriendInfo()</code>}}
```