# API UnitHasIncomingResurrection

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Returns true if the unit is currently being resurrected.
 isBeingResurrected = UnitHasIncomingResurrection(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - either the unitID ("player", "target", "party3", etc) or unit's name ("Bob" or "Bob-Llane")

==Returns==
:;isBeingResurrected:{{apitype|boolean}} - Returns true if the unit is being resurrected by any means, be it spell, item, or some other method. Returns nil/false otherwise.

==Details==
* This returns nil/false if the cast is completed and the unit has not yet accepted the resurrection. It is only true if the cast is in progress and the cast is some method of resurrection.

==Patch changes==
* {{Patch 4.2.0|note=Added.}}
```