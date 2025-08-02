# API C BattleNet.GetFriendGameAccountInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_BattleNet|system=BattleNet}}
Returns information on the game the Battle.net friend is playing.
 gameAccountInfo = C_BattleNet.GetFriendGameAccountInfo(friendIndex, accountIndex)
                 = C_BattleNet.GetGameAccountInfoByID(id)
                 = C_BattleNet.GetGameAccountInfoByGUID(guid)

==Arguments==
===<font color="#4ec9b0">GetFriendGameAccountInfo</font>===
:;friendIndex:{{apitype|number}} - Index ranging from 1 to {{api|BNGetNumFriends}}()
:;accountIndex:{{apitype|number}} - Index ranging from 1 to {{api|C_BattleNet.GetFriendNumGameAccounts}}()

===<font color="#4ec9b0">GetGameAccountInfoByID</font>===
:;id:{{apitype|number}} : <code>gameAccountInfo.gameAccountID</code>

===<font color="#4ec9b0">GetGameAccountInfoByGUID</font>===
:;guid:{{apitype|string}} : [[GUID|UnitGUID]]

==Returns==
[[Image:API_C_BattleNet.GetFriendGameAccountInfo.png|frame|right|[https://github.com/TekNoLogic/Spew /spew] output]]
:;gameAccountInfo:{{apitype|BNetGameAccountInfo?}}
{{:Struct BNetGameAccountInfo|nocaption=1}}

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|C_BattleNet.GetFriendAccountInfo}} }}
|}

==Example==
* Shows your Battle.net friends' game information. Tested with one friend online in the mobile app, and one friend offline.
<syntaxhighlight lang="lua">
for i = 1, BNGetNumFriends() do
	for j = 1, C_BattleNet.GetFriendNumGameAccounts(i) do
		local game = C_BattleNet.GetFriendGameAccountInfo(i, j)
		print(game.gameAccountID, game.isOnline, game.clientProgram)
	end
end
-- 5, true, "BSAp"
</syntaxhighlight>

* <code>C_BattleNet.GetFriendAccountInfo()</code> returns the same information in <code>gameAccountInfo</code>
<syntaxhighlight lang="lua">
for i = 1, BNGetNumFriends() do
	local game = C_BattleNet.GetFriendAccountInfo(i).gameAccountInfo
	print(game.gameAccountID, game.isOnline, game.clientProgram)
end
-- 5, true, "BSAp"
-- nil, false, ""
</syntaxhighlight>

==Patch changes==
* {{Patch 8.2.5|note=Changed to <code>C_BattleNet.GetFriendGameAccountInfo</code> and <code>C_BattleNet.GetGameAccountInfoByID()</code>.<sup>[https://www.townlong-yak.com/framexml/8.2.5/Blizzard_Deprecated/Deprecated_8_2_5.lua#113]</sup>}}
* {{Patch 6.2.4|note=Changed to {{api|BNGetFriendGameAccountInfo}}() and {{api|BNGetGameAccountInfo}}().}}
* {{Patch 3.3.5|note=Added as <code>BNGetFriendToonInfo()</code> and <code>BNGetToonInfo()</code>.}}
```