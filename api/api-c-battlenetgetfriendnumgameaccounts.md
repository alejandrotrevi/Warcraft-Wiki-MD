# API C BattleNet.GetFriendNumGameAccounts

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_BattleNet|system=BattleNet}}
Returns the number of game accounts for the Battle.net friend.
 numGameAccounts = C_BattleNet.GetFriendNumGameAccounts(friendIndex)

==Arguments==
:;friendIndex:{{apitype|number}} - The Battle.net friend's index on the friends list ranging from 1 to {{api|BNGetNumFriends}}()

==Returns==
:;numGameAccounts:{{apitype|number}} - The number of accounts or 0 if friend is not online.

==Details==
* This function returns the number of ACCOUNTS a player has that are identified with a given battletag ID rather than the number of characters on a given account.

==Patch changes==
* {{Patch 8.2.5|note=Changed to <code>C_BattleNet.GetFriendNumGameAccounts()</code>}}
* {{Patch 6.2.4|note=Changed to <code>BNGetNumFriendGameAccounts()</code>}}
* {{Patch 3.3.3|note=Added as <code>BNGetNumFriendToons()</code>}}
```