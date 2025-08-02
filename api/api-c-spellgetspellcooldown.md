# API C Spell.GetSpellCooldown

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns the cooldown info of a spell.
 spellCooldownInfo = C_Spell.GetSpellCooldown(spellIdentifier)

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}} - Spell ID, name, name(subtext), or link

==Returns==
:;spellCooldownInfo:{{apitype|SpellCooldownInfo?}} - Returns nil if spell is not found
{{:Struct SpellCooldownInfo|nocaption=1}}

==Details==
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|SPELL_UPDATE_COOLDOWN}} }}
|}
* To check the [[Global Cooldown]], you can use the spell ID <code>61304</code>. This is a dummy spell specifically for the GCD.
* The enabled return value allows addons to easily check if the player has used a buff-providing spell (such as Presence of Mind or Nature's Swiftness) without searching through the player's buffs.
* Values returned by this function are not updated immediately when {{api|t=e|UNIT_SPELLCAST_SUCCEEDED}} event is raised.

==Patch changes==
* {{Patch 11.0.0|note=Added, replacement for {{api|GetSpellCooldown}}.}}
```