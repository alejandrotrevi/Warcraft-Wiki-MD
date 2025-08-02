# API GetInspectSpecialization

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the specialization for the inspected player unit.
 id = GetInspectSpecialization(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The player to inspect.

==Returns==
:;id:{{apitype|number}} - [[SpecializationID]].

==Details==
* Requires calling {{api|NotifyInspect}}() and awaiting {{api|t=e|INSPECT_READY}}; returns 0 until inspect info is available.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```