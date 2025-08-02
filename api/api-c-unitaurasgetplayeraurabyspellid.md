# API C UnitAuras.GetPlayerAuraBySpellID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about an aura on the player by a given spell ID.
 aura = C_UnitAuras.GetPlayerAuraBySpellID(spellID)

==Arguments==
:;spellID:{{apitype|number}} - The spell ID to query.

==Returns==
:;aura:{{apitype|AuraData?}} - Structured information about the found aura, if any.
{{:Struct_AuraData|nocaption=1}}

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```