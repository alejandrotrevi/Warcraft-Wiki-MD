# API CanSummonFriend

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6}}
Returns whether you can RaF summon a particular unit.
 summonable = CanSummonFriend(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The player to check whether you can summon.

==Returns==
:;summonable:{{apitype|boolean}} - 1 if you can summon the unit using RaF, nil otherwise.

==Example==
The snippet below checks whether you can summon the target, and, if so, whispers and summons her to you.
 local t = "target"; 
 if CanSummonFriend(t) then 
   SendChatMessage("I am summoning you!","WHISPER",nil,t) 
   SummonFriend(t) 
 end
```