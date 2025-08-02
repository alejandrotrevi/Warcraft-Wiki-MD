# API UnitDefense

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the [[defense]] of the unit without [[armor]], and defense value of their armor.

:For NPCs and pets, it will return a baseDefense value, though armorDefense will be 0.
:For other player targets than "player", it will return 0 for baseDefense and 0 for armorDefense.

 baseDefense, armorDefense = UnitDefense(unit);

----
;''Arguments''

:;unit:{{apitype|string}} : [[UnitId]] - Only <code>"player"</code> is supported

----
;''Returns''

:baseDefense, armorDefense
:;baseDefense:{{apitype|number}} - The unit's defense without armor. Includes the warrior talent Anticipation.
:;armorDefense:{{apitype|number}} - The defense gained from the unit's armor.

----
;''Example''
 local  baseDefense, armorDefense = UnitDefense("player");

;''Result''

----
;''Description''

: Returns the defense statistics of the player.
```