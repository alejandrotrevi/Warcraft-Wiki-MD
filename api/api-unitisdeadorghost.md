# API UnitIsDeadOrGhost

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns true if the unit is dead or in ghost form.
 isDeadOrGhost = UnitIsDeadOrGhost(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;isDeadOrGhost:{{apitype|boolean}}

==Details==
* Effectively combines {{api|UnitIsDead}} and {{api|UnitIsGhost}}, returning true if ''either'' of those functions would return true.
* Does not work for despawned pet units. (A pet is "despawned" once its corpse is no longer targetable in the game world, or its action bar is no longer visible on its owner's screen.)
* Returns false for priests who are currently in [[Spirit of Redemption]] form, having died once and are about to die again.

==See also==
* {{api|UnitIsDead}}
* {{api|UnitIsGhost}}
```