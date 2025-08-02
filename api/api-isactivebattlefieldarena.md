# API IsActiveBattlefieldArena

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the player is inside a (rated) arena.
 isArena, isRegistered = IsActiveBattlefieldArena()

==Returns==
:;isArena:{{apitype|boolean}} - If the player is inside an arena.
:;isRegistered:{{apitype|boolean}} - If the player is playing a rated arena match.

==Details==
* If you are in waiting room and/or countdown is going on, it will return false.
```