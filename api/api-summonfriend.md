# API SummonFriend

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6}}
Summons a player using the RaF system.
 SummonFriend(guid, name)

==Arguments==
:;guid:{{apitype|string}} : [[GUID#Player|GUID]] - The guid of the player.
:;name:{{apitype|string}} - The name of the player.

==Example==
Summons the current target if the target is a recruited friend.
<syntaxhighlight lang="lua">
SummonFriend(UnitGUID("target"), UnitName("target"))
</syntaxhighlight>

==See also==
* {{api|CanSummonFriend}}
* {{api|GetSummonFriendCooldown}}
```