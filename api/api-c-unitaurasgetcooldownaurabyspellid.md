# API C UnitAuras.GetCooldownAuraBySpellID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Obtains the spell ID of a passive cooldown effect associated with a spell.
 passiveCooldownSpellID = C_UnitAuras.GetCooldownAuraBySpellID(spellID)

==Arguments==
:;spellID:{{apitype|number}} - The spell ID to query.

==Returns==
:;passiveCooldownSpellID:{{apitype|number?}} - The spell ID of an associated passive aura effect, if any.

==Details==
* This API is used in conjunction with [[API C UnitAuras.GetPlayerAuraBySpellID|C_UnitAuras.GetPlayerAuraBySpellID]] to display passive effect cooldowns on action buttons.

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```