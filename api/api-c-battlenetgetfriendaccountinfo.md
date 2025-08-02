# API C BattleNet.GetFriendAccountInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_BattleNet|system=BattleNet}}
Returns information about a Battle.net friend account.
 accountInfo = C_BattleNet.GetFriendAccountInfo(friendIndex [, wowAccountGUID])
             = C_BattleNet.GetAccountInfoByID(id [, wowAccountGUID])
             = C_BattleNet.GetAccountInfoByGUID(guid)

==Arguments==
===<font color="#4ec9b0">GetFriendAccountInfo</font>===
:;friendIndex:{{apitype|number}} - Index ranging from 1 to {{api|BNGetNumFriends}}()
:;wowAccountGUID:{{apitype|string?}} : [[GUID#BNetAccount|BNetAccountGUID]]

===<font color="#4ec9b0">GetAccountInfoByID</font>===
:;id:{{apitype|number}} : bnetAccountID
:;wowAccountGUID:{{apitype|string?}} : [[GUID#BNetAccount|BNetAccountGUID]]

===<font color="#4ec9b0">GetAccountInfoByGUID</font>===
:;guid:{{apitype|string}} : [[GUID#Player|UnitGUID]]

==Returns==
[[Image:API_C_BattleNet.GetFriendAccountInfo.png|frame|right|[https://github.com/TekNoLogic/Spew /spew] output]]
:;accountInfo:{{apitype|BNetAccountInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|bnetAccountID}} || {{apitype|number}} || A temporary ID for the friend's battle.net account during this session
|-
| {{apiname|accountName}} || {{apitype|string}} || A [[UI_escape_sequences#Protected_strings|protected string]] representing the friend's full name or BattleTag name.
|-
| {{apiname|battleTag}} || {{apitype|string}} || The friend's [[BattleTag]] (e.g., "Nickname#0001")
|-
| {{apiname|isFriend}} || {{apitype|boolean}} || 
|-
| {{apiname|isBattleTagFriend}} || {{apitype|boolean}} || 
|-
| {{apiname|lastOnlineTime}} || {{apitype|number}} || The number of seconds elapsed since this friend was last online (from the epoch date of January 1, 1970). Returns nil if currently online.
|-
| {{apiname|isAFK}} || {{apitype|boolean}} || Whether or not the friend is flagged as Awayther or not the friend is flagged as Busy
|-
| {{apiname|isDND}} || {{apitype|boolean}} || Whether or not the friend is flagged as Busy
|-
| {{apiname|isFavorite}} || {{apitype|boolean}} || Whether or not the friend is marked as a favorite by you
|-
| {{apiname|appearOffline}} || {{apitype|boolean}} || 
|-
| {{apiname|customMessage}} || {{apitype|string}} || The Battle.net broadcast message
|-
| {{apiname|customMessageTime}} || {{apitype|number}} || The number of seconds elapsed since the current broadcast message was sent
|-
| {{apiname|note}} || {{apitype|string}} || The contents of the player's note about this friend
|-
| {{apiname|rafLinkType}} || {{apitype|Enum.RafLinkType}} || 
|-
| {{apiname|gameAccountInfo}} || {{apitype|BNetGameAccountInfo}} || 
|}

{{:Struct BNetGameAccountInfo}}

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|C_BattleNet.GetFriendGameAccountInfo}} }}
|}

==Example==
Shows your own account info.
 /dump C_BattleNet.GetAccountInfoByID(select(3, {{api|BNGetInfo}}()))

Shows your Battle.net friends' account information.
<syntaxhighlight lang="lua">
for i = 1, BNGetNumFriends() do
	local acc = C_BattleNet.GetFriendAccountInfo(i)
	local game = acc.gameAccountInfo
	print(acc.bnetAccountID, acc.accountName, game.gameAccountID, game.isOnline, game.clientProgram)
end
-- 1, "|Kq2|k", 5, true, "BSAp"
-- 2, "|Kq1|k", nil, false, ""
</syntaxhighlight>

==Patch changes==
* {{Patch 11.0.5|note=Removed <code>isWowMobile</code> field.}}
* {{Patch 8.2.5|note=Changed to <code>C_BattleNet.GetFriendAccountInfo()</code> and <code>C_BattleNet.GetAccountInfoByID()</code>.<sup>[https://www.townlong-yak.com/framexml/8.2.5/Blizzard_Deprecated/Deprecated_8_2_5.lua#71]</sup>}}
* {{Patch 6.2.4|note=Replaced <code>presenceID</code> and <code>presenceName</code> with <code>bnetIDAccount</code> and <code>accountName</code>.}}
* {{Patch 5.0.4|note=Replaced <code>givenName</code> and <code>surname</code> with <code>presenceName</code>, <code>battleTag</code>, and <code>isBattleTagPresence</code>.}}
* {{Patch 3.3.5|note=Added as {{api|BNGetFriendInfo}}() and {{api|BNGetFriendInfoByID}}().}}
```