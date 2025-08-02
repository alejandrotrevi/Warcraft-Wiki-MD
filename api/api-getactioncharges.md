# API GetActionCharges

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the charges of a charge-accumulating player ability.
 currentCharges, maxCharges, cooldownStart, cooldownDuration, chargeModRate = GetActionCharges(slot)

==Arguments==
:;slot:{{apitype|number}} - The [[ActionSlot|action slot]] to retrieve data from.

==Returns==
:;currentCharges:{{apitype|number}} - The number of charges of the ability currently available.
:;maxCharges:{{apitype|number}} - The maximum number of charges the ability may have available.
:;cooldownStart:{{apitype|number}} - Time (per {{api|GetTime}}) at which the next charge cooldown began, or <code>2^32 / 1000</code> if the spell is not currently recharging.
:;cooldownDuration:{{apitype|number}} - Time (in seconds) required to gain a charge.
:;chargeModRate:{{apitype|number}} - The rate at which the charge cooldown widget's animation should be updated.

==Details==
* Abilities like [[Roll (monk ability)]] can be used by the player rapidly, and then slowly accumulate charges over time. The <code>cooldownStart</code> and <code>cooldownDuration</code> return values indicate the cooldown timer for the acquiring next charge (when <code>currentCharges</code> is less than <code>maxCharges</code>).
* If the queried spell does not accumulate charges over time (e.g. [[Arcane Missiles]] or [[Jab]]), this function does not return any values.

==Patch changes==
* {{Patch 7.1.0|note=The <code>chargeModRate</code> return value was added.}}
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|GetSpellCharges()}} - Referring to any spell ID or localized spell name.
```