# API CanJoinBattlefieldAsGroup

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns true if the player can join a battlefield with a group.
 isTrue = CanJoinBattlefieldAsGroup()

==Returns==
:;isTrue:{{apitype|boolean}} - returns true, if the player can join the battlefield as group

==Example==
 if(CanJoinBattlefieldAsGroup()) then
  JoinBattlefield(0,1) -- join battlefield as group
 else
  JoinBattlefield(0,0) -- join battlefield as single player
 end

<big>'''Result'''</big>

Queries the player either as group or as single player.
```