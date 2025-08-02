# API BNGetNumFriendGameAccounts

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the specified Battle.net friend's number of toons.

 numGameAccounts = BNGetNumFriendGameAccounts(friendIndex)

==Arguments==
:;friendIndex:{{apitype|number}} - The Battle.net friend's index on the friendslist

==Returns==
:;numGameAccounts:{{apitype|number}} - The number of accounts or 0 if friend is not online.

==Details==
: This function returns the number of ACCOUNTS a player has that are identified with a given battletag ID rather than the number of characters on a given account.

==Patch changes==
* {{Patch 6.2.4|note=Name changed from BNGetNumFriendToons.}}
```