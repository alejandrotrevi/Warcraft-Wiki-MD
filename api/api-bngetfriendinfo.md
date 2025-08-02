# API BNGetFriendInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the specified RealID friend.
 bnetAccountID, accountName, battleTag, isBattleTagPresence, characterName, bnetIDGameAccount, client, isOnline, lastOnline, isAFK, isDND, messageText, noteText, isRIDFriend, messageTime, canSoR, isReferAFriend, canSummonFriend
     = BNGetFriendInfo(friendIndex)
     = BNGetFriendInfoByID(bnetAccountID)

==Arguments==
===<font color="#4ec9b0">BNGetFriendInfo</font>===
:;friendIndex:{{apitype|number}} - The index on the friends list for this RealID friend, ranging from 1 to {{api|BNGetNumFriends}}()
===<font color="#4ec9b0">BNGetFriendInfoByID</font>===
:;bnetAccountID:{{apitype|number}} - A unique numeric identifier for this friend's battle.net account for the current session

==Returns==
:;bnetAccountID:{{apitype|number}} - A temporary ID for the friend's battle.net account during this session.
:;accountName:{{apitype|string}} - An [[UI escape sequences|escape sequence]] (starting with |K) representing the friend's full name or BattleTag name.
:;battleTag:{{apitype|string}} - A nickname and number that when combined, form a unique string that identifies the friend (e.g., "Nickname#0001").
:;isBattleTagPresence:{{apitype|boolean}} - Whether or not the friend is known by their BattleTag.
:;characterName:{{apitype|string}} - The name of the logged in character.
:;bnetIDGameAccount:{{apitype|number}} - A unique numeric identifier for the friend's game account during this session.
:;client:{{apitype|string}} - See BNET_CLIENT
:;isOnline:{{apitype|boolean}} - Whether or not the friend is online.
:;lastOnline:{{apitype|number}} - The number of seconds elapsed since this friend was last online (from the epoch date of January 1, 1970). Returns nil if currently online.
:;isAFK:{{apitype|boolean}} - Whether or not the friend is flagged as Away.
:;isDND:{{apitype|boolean}} - Whether or not the friend is flagged as Busy.
:;messageText:{{apitype|string}} - The friend's Battle.Net broadcast message.
:;noteText:{{apitype|string}} - The contents of the player's note about this friend.
:;isRIDFriend:{{apitype|boolean}} - Returns true for RealID friends and false for BattleTag friends.
:;messageTime:{{apitype|number}} - The number of seconds elapsed since the current broadcast message was sent.
:;canSoR:{{apitype|boolean}} - Whether or not this friend can receive a [[Scroll of Resurrection]].
:;isReferAFriend:{{apitype|boolean}}
:;canSummonFriend:{{apitype|boolean}}

==Details==
{{:Const_BNET_CLIENT}}

==Patch changes==
* {{Patch 6.2.4|note=Replaced <code>presenceID</code> and <code>presenceName</code> with <code>bnetIDAccount</code> and <code>accountName</code>.}}
* {{Patch 5.0.4|note=Replaced <code>givenName</code> and <code>surname</code> with <code>presenceName</code>, <code>battleTag</code>, and <code>isBattleTagPresence</code>.}}

==See also==
* {{api|BNGetFriendGameAccountInfo}}
* {{api|BNGetGameAccountInfo}}
```