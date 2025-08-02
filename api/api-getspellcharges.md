# API GetSpellCharges

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=11.0.0|removed=11.0.2}}
Returns information about the charges of a charge-accumulating player ability.
 currentCharges, maxCharges, cooldownStart, cooldownDuration, chargeModRate
     = GetSpellCharges(spell)
     = GetSpellCharges(index, bookType)
==Arguments==
{{:SpellArg}}

==Returns==
:;currentCharges:{{apitype|number}} - The number of charges of the ability currently available.
:;maxCharges:{{apitype|number}} - The maximum number of charges the ability may have available.
:;cooldownStart:{{apitype|number}} - Time (per {{api|GetTime}}) at which the last charge cooldown began, or <code>2^32 / 1000</code> - cooldownDuration if the spell is not currently recharging.
:;cooldownDuration:{{apitype|number}} - Time (in seconds) required to gain a charge.
:;chargeModRate:{{apitype|number}} - The rate at which the charge cooldown widget's animation should be updated.

==Details==
* Abilities like [[Roll (monk ability)]] can be used by the player rapidly, and then slowly accumulate charges over time. The <code>cooldownStart</code> and <code>cooldownDuration</code> return values indicate the cooldown timer for the acquiring next charge (when <code>currentCharges</code> is less than <code>maxCharges</code>).
* If the queried spell does not accumulate charges over time (e.g. [[Arcane Missiles]] or [[Jab]]), this function does not return any values.
*Targeted dispels like [[Purify]] or [[Cleanse Spirit]] hold one hidden charge which may be queried with GetSpellCharges. The spells will immediately—or after a few in-game ticks—regain their charge if cast on a friendly unit that could not be dispelled. This may cause sporadic behavior when tracking cooldowns, because upon raising SPELL_UPDATE_COOLDOWN, the function [[API GetSpellCooldown]] will momentarily return that the spell is on it's full cooldown duration.

==Patch changes==
* {{Patch 7.1.0|note=The <code>chargeModRate</code> return value was added.}}

==See also==
* {{api|GetActionCharges(slot)}} - Referring to a button on an action bar.
```