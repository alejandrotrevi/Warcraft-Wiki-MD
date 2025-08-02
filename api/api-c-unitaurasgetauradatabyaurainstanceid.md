# API C UnitAuras.GetAuraDataByAuraInstanceID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about an aura on a unit by a given aura instance ID.
 aura = C_UnitAuras.GetAuraDataByAuraInstanceID(unit, auraInstanceID)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit to query.
:;auraInstanceID:{{apitype|number}} - An aura instance ID.

==Returns==
:;aura:{{apitype|UnitAuraInfo?}} - Structured information about the found aura, if any.
{{:Struct_UnitAuraInfo|nocaption=1}}

==Details==
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|UNIT_AURA}} }}
|}

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```