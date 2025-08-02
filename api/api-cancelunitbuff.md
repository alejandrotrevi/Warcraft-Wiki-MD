# API CancelUnitBuff

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 4.0.1; Use <code>/cancelaura Buff Name</code> in macros, or [[SecureAuraHeaderTemplate]] if re-implementing buff frames.}}
Removes a specific buff from the character.
 CancelUnitBuff(unit, buffIndex [, filter])

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit to cancel the buff from, must be under the player's control.
:;buffIndex:{{apitype|number}} - index of the buff to cancel, ascending from 1.
:;filter:{{apitype|string?}} - any of combination of "HELPFUL|HARMFUL|PLAYER|RAID|CANCELABLE|NOT_CANCELABLE".

==Details==
* This function does not work for canceling druid forms, rogue Stealth, death knight presences, or priest Shadowform.

==Patch changes==
* {{Patch 8.0.1|note=Removed ability to cancel by name and rank. Functionality replaced by {{api|CancelSpellByName}}.}}
* {{Patch 4.0.1|note=Protected while in combat; tainted code cannot cancel stance-affecting buffs even while out of combat.}}
* {{Patch 3.0.2|note=Replaced {{api|CancelPlayerBuff}}.}}
```