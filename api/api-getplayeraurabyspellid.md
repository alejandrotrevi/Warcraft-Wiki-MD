# API GetPlayerAuraBySpellID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns an active buff/debuff by spell ID on the player character.
 name, icon, count, dispelType, duration, expirationTime, source, isStealable, nameplateShowPersonal,
 spellId, canApplyAura, isBossDebuff, castByPlayer, nameplateShowAll, timeMod, ...
     = GetPlayerAuraBySpellID(spellID)

==Arguments==
:;spellID:{{apitype|number}}

==Returns==
: Returns <code>nil</code> if there is no active aura with that spell ID.
<onlyinclude>{{AuraType|aura}}</onlyinclude>

==Details==
* The advantage over {{api|UnitAura}}() is this function does not require iterating over a list of auras for a specific Spell ID.
* If two spells of the same ID are active, then the first applied one will be returned until it expires and then the second applied one.

==Example==
Returns if the player has the [https://www.wowhead.com/spell=21562/power-word-fortitude Power Word: Fortitude] buff
 /dump GetPlayerAuraBySpellID(21562)

==Patch changes==
* {{Patch 9.2.5|note=The GetPlayerAuraBySpellID() API no longer returns information about hidden auras.<sup>[https://github.com/Gethe/wow-ui-source/blob/9.2.5/Interface/AddOns/Blizzard_Deprecated/Deprecated_9_2_5.lua#L27]</sup>}}
* {{Patch 9.0.1|note=Added.}}

{{apinavbox|UnitAura}}
```