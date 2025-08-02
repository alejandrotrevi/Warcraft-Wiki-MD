# API BNGetFriendGameAccountInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the specified toon of a RealID friend.
 hasFocus, characterName, client, realmName, realmID, faction, race, class, guild, zoneName, level, gameText, broadcastText, broadcastTime, canSoR, toonID, bnetIDAccount, isGameAFK, isGameBusy
     = BNGetFriendGameAccountInfo(friendIndex)
     = BNGetGameAccountInfo(bnetIDGameAccount)
     = BNGetGameAccountInfoByGUID(guid)
==Arguments==
===<font color="#4ec9b0">BNGetFriendGameAccountInfo</font>===
:;friendIndex:{{apitype|number}} - Ranging from 1 to {{api|BNGetNumFriendGameAccounts}}()
===<font color="#4ec9b0">BNGetGameAccountInfo</font>===
:;bnetIDGameAccount:{{apitype|number}} - A unique numeric identifier for the friend during this session.
===<font color="#4ec9b0">BNGetGameAccountInfoByGUID</font>===
:;guid:{{apitype|string}}

==Returns==
:;hasFocus:{{apitype|boolean}} - Whether or not this toon is the one currently being displayed in Blizzard's FriendFrame.
:;characterName:{{apitype|string}} - The name of the logged in toon/character.
:;client:{{apitype|string}} - Either "WoW" (BNET_CLIENT_WOW), "S2" (BNET_CLIENT_S2), "WTCG" (BNET_CLIENT_WTCG), "App" (BNET_CLIENT_APP), "Hero" (BNET_CLIENT_HEROES), "Pro" (BNET_CLIENT_OVERWATCH), "CLNT" (BNET_CLIENT_CLNT), or "D3" (BNET_CLIENT_D3) for World of Warcraft, StarCraft 2, Hearthstone, BNet Application, Heroes of the Storm, Overwatch, another client, or Diablo 3.
:;realmName:{{apitype|string}} - The name of the logged in realm.
:;realmID:{{apitype|number}} - The ID for the logged in realm.
:;faction:{{apitype|string}} - The faction name (i.e., "Alliance" or "Horde").
:;race:{{apitype|string}} - The localized race name (e.g., "Blood Elf").
:;class:{{apitype|string}} - The localized class name (e.g., "Death Knight").
:;guild:{{apitype|string}} - Seems to return "" even if the player is in a guild.
:;zoneName:{{apitype|string}} - The localized zone name (e.g., "The Undercity").
:;level:{{apitype|string}} - The current level (e.g., "90").
:;gameText:{{apitype|string}} - For WoW, returns "<code>zoneName</code> - <code>realmName</code>". For StarCraft 2 and Diablo 3, returns the location or activity the player is currently engaged in.
:;broadcastText:{{apitype|string}} - The Battle.Net broadcast message.
:;broadcastTime:{{apitype|number}} - The number of seconds elapsed since the current broadcast message was sent.
:;canSoR:{{apitype|boolean}} - Whether or not this friend can receive a [[Scroll of Resurrection]].
:;toonID:{{apitype|number}} - A unique numeric identifier for the friend's character during this session.
:;bnetIDAccount:{{apitype|number}}
:;isGameAFK:{{apitype|boolean}}
:;isGameBusy:{{apitype|boolean}}

==Example==
<syntaxhighlight lang="lua">
local bnetIDGameAccount = select(6,BNGetFriendInfo(1)) -- assuming friend index 1 is me (Grdn)
local _, characterName, _, realmName = BNGetGameAccountInfo(bnetIDGameAccount)
print(toonName.." plays on "..realmName) -- Grdn plays on Onyxia
</syntaxhighlight>

==Patch changes==
* {{Patch 6.2.4|note=API Changed from BNGetToonInfo to BNGetGameAccountInfo.}}
* {{Patch 5.0.4|note=Returns changed: <code>faction</code> is now a string. <code>canSoR</code> and <code>toonID</code> added.}}
```