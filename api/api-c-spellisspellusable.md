# API C Spell.IsSpellUsable

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns whether the spell is currently castable.
 isUsable, insufficientPower = C_Spell.IsSpellUsable(spellIdentifier)

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}} - Spell ID, name, name(subtext), or link

==Returns==
:;isUsable:{{apitype|boolean}} - True if the spell is usable, false otherwise
:;insufficientPower:{{apitype|boolean}} - True if spell is specifically unusable due to insufficient power (i.e. MANA, RAGE, etc)

==Details==
* A spell might be unusable for a variety of reasons, such as:
:* The player hasn't learned the spell.
:* The player lacks required mana or reagents.
:* Reactive conditions haven't been met.

==Patch changes==
* {{Patch 11.0.0|note=Added, replacement for {{api|IsUsableSpell}}.}}
```