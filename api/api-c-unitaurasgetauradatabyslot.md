# API C UnitAuras.GetAuraDataBySlot

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about an aura on a unit by a given slot index.
 aura = C_UnitAuras.GetAuraDataBySlot(unit, slot)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit to query.
:;slot:{{apitype|number}} - A slot index obtained from the variable returns of [[API UnitAuraSlots|UnitAuraSlots]].

==Returns==
:;aura:{{apitype|UnitAuraInfo?}} - Structured information about the found aura, if any.
{{:Struct_UnitAuraInfo|nocaption=1}}

==Details==
* This API can be used as an alternative to [[API UnitAuraBySlot|UnitAuraBySlot]] to obtain information about the aura in a structured table.

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```