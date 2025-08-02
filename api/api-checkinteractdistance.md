# API CheckInteractDistance

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 10.2.0.}}
Returns true if the player is in range to perform a specific interaction with the unit.
 inRange = CheckInteractDistance(unit, distIndex)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit to compare distance to.
:;distIndex:{{apitype|number}} - A value from 1 to 5:
::1 = Compare Achievements, 28 yards
::2 = Trade, 8 yards
::3 = Duel, 7 yards
::4 = Follow, 28 yards
::5 = Pet-battle Duel, 7 yards

==Returns==
:;inRange:{{apitype|boolean}} - 1 if you are in range to perform the interaction, nil otherwise.

==Details==
* If "unit" is a hostile unit, the return values are the same.  But you obviously won't be able to do things like Trade.

==Example==
 if ( CheckInteractDistance("target", 4) ) then
   FollowUnit("target");
 else
   -- we're too far away to follow the target
 end

==Patch changes==
* {{Hotfix|date=2023-12-11|doc=|version=10.2.0.52485|note=Partially unrestricted. Querying enemy units while in combat is once again permitted.}}
* {{Hotfix|date=2023-11-16|version=10.2.0.52188|note=Protected. May no longer be called in combat by insecure code.}}
```