# API GetFriendInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieves information about a person on your friends list.
 name, level, class, area, connected, status, note, isReferAFriend, guid = GetFriendInfo(friendIndex)

==Arguments==
:;friendIndex : Integer - Index of friend in the friend list (Note that status changes can re-order the friend list, indexes are not guaranteed to remain stable across events) (Also note that index should not be greater than 50 [see Notes]).

==Returns==
:;name : String - Friend's name, or nil (if index is invalid)
:;level : Integer - Friend's level, or 0 (if offline/invalid).
:;class : String - Friend's class, or "Unknown" (if offline/invalid).
:;area : String - Friend's current location, or "Unknown" (if offline/invalid).
:;connected : Boolean - true if friend is online, false otherwise.
:;status : String - Friend's current status flags (AFK or DND).
:;note : String - Friends note, or nil
:;isReferAFriend : Boolean - true is Refer-A-Friend
:;guid : String - a string containing the hexadecimal representation of the player's [[GUID]]. Player-[server ID]-[player UID] (Example: "Player-976-0002FD64")

==Example==
This example is pre-2.4 and thus doesn't utilize the friend note.
 local name, level, class, loc, connected, status = GetFriendInfo(1);
 if (name) then
  DEFAULT_CHAT_FRAME:AddMessage("Your "..status.." friend "..name.." (The level "..level.." "..class..") is in "..loc..".");
 else
  DEFAULT_CHAT_FRAME:AddMessage("You have no friends?!");
 end
===Result===
Your <AFK> friend Bill (The level 99 Leprechaun) is in Neverland.

==Notes==
Friend information isn't necessarily automatically kept up to date. You can use the [[API ShowFriends|ShowFriends]] function to request an update from the server.


Do not use indexes greater than 50 (the maximum number of friend list entries)!

With some AddOns installed the client may crash after typing "/script GetFriendInfo(51)" (especially if FlagRSP is activated).

This crash leads to ERROR #132 (memory could not be "read").

Please use GetNumFriends() to iterate over all indexes securely.

==References==
{{Elink|icon=wowus|link=http://forums.worldofwarcraft.com/thread.html?topicId=5835557417#1|site="ACTUAL API Changes - 2.3.3 to 2.4.1" - Forum post by Iriel (UI and Macros Forum MVP)}}
```