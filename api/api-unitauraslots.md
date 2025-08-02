# API UnitAuraSlots

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.5|removed=11.0.2}}
Returns an ordered list of auras used with {{api|UnitAuraBySlot()}}
 continuationToken, ... = UnitAuraSlots(unit, filter [, maxSlots, continuationToken])

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]
:;filter:{{apitype|string}} - Similar to {{api|UnitAura}}; however, either "HELPFUL" or "HARMFUL" is required.
:;maxSlots:{{apitype|number?}} - The maximum number of slots to return
:;continuationToken:{{apitype|number?}} - The number of slots to skip.

==Returns==
:;continuationToken:{{apitype|number?}} - Indicates that maxSlots was reached.
:;...:{{apitype|number}} - A batch of slots used with {{api|UnitAuraBySlot}}()

==Details==
{{:API_UnitAuraBySlot}}

==Patch changes==
* {{Patch 10.2.5|note=Deprecated. Replaced by {{api|t=a|C_UnitAuras.GetAuraSlots}}.}}
* {{Patch 8.2.5|note=Added.}}

{{apinavbox|UnitAura}}
```