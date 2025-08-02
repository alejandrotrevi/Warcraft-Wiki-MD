# API BNGetNumFriends

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the amount of (online) Battle.net friends.
 numBNetTotal, numBNetOnline, numBNetFavorite, numBNetFavoriteOnline = BNGetNumFriends()

==Returns==
:;numBNetTotal:{{apitype|number}} - amount of Battle.net friends on the friends list
:;numBNetOnline:{{apitype|number}} - online Battle.net friends
:;numBNetFavorite:{{apitype|number}} - favorite battle.net friends
:;numBNetFavoriteOnline:{{apitype|number}} - favorite online battle.net friends

==Example==
<syntaxhighlight lang="lua">
local total, online = BNGetNumFriends()
print("You have "..total.." Battle.net friends and "..online.." of them are online!")
</syntaxhighlight>

==Patch changes==
* {{Patch 8.2.0|note=Added numBNetFavorite and numBNetFavoriteOnline. This fixes the friends list sorting.}}
* {{Patch 3.3.5|note=Added.}}
```