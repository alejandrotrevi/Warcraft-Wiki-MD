# API GetSpellCooldown

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=11.0.0|removed=11.0.2}}
Returns the cooldown info of a spell.
 start, duration, enabled, modRate = GetSpellCooldown(spell)
                                   = GetSpellCooldown(index, bookType)

==Arguments==
{{:SpellArg}}

==Returns==
:;startTime:{{apitype|number}} - The time when the cooldown started (as returned by [[API GetTime|GetTime()]]); zero if no cooldown; current time if (enabled == 0).
:;duration:{{apitype|number}} - Cooldown duration in seconds, 0 if spell is ready to be cast.
:;enabled:{{apitype|number}} - 0 if the spell is active (Stealth, Shadowmeld, Presence of Mind, etc) and the cooldown will begin as soon as the spell is used/cancelled; 1 otherwise.
:;modRate:{{apitype|number}} - The rate at which the cooldown widget's animation should be updated.

==Details==
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|SPELL_UPDATE_COOLDOWN}} }}
|}
* To check the [[Global Cooldown]], you can use the spell ID <code>61304</code>. This is a dummy spell specifically for the GCD.
* The enabled return value allows addons to easily check if the player has used a buff-providing spell (such as Presence of Mind or Nature's Swiftness) without searching through the player's buffs.
* Values returned by this function are not updated immediately when {{api|t=e|UNIT_SPELLCAST_SUCCEEDED}} event is raised.

==Example==
The following snippet checks the state of [[Presence of Mind]] cooldown. On English clients, you could also use <code>"Presence of Mind"</code> in place of <code>12043</code>, which is the spell's ID.
 local start, duration, enabled, modRate = GetSpellCooldown(12043)
 if enabled == 0 then
  print("Presence of Mind is currently active, use it and wait " .. duration .. " seconds for the next one.")
 elseif ( start > 0 and duration > 0) then
  local cdLeft = start + duration - GetTime()
  print("Presence of Mind is cooling down, wait " .. cdLeft .. " seconds for the next one.")
 else
  print("Presence of Mind is ready.")
 end

==Patch changes==
* {{Patch 11.0.0|note=Removed, replaced by {{api|C_Spell.GetSpellCooldown}} and {{api|C_SpellBook.GetSpellBookItemCooldown}}.}}
* {{Patch 7.1.0|note=The <code>modRate</code> return value was added.}}
* {{Patch 6.2.0|note=The <code>charges</code> and <code>maxCharges</code> return values were removed. They were moved to [[API GetSpellCharges|GetSpellCharges]].}}
```