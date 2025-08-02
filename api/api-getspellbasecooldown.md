# API GetSpellBaseCooldown

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gives the (unmodified) cooldown and global cooldown of an ability in milliseconds.
 cooldownMS, gcdMS = GetSpellBaseCooldown(spellid)

==Arguments==
:;spellid:{{apitype|number}} - The spellid of your ability.

==Returns==
:;cooldownMS:{{apitype|number}} - Millisecond duration of the spell's cooldown (if any other than the global cooldown)
:;gcdMS:{{apitype|number}} - Millisecond duration of the spell's global cooldown (if any)

==Note==
Polling the second return value will discover if a particular spell is subject to GCD.

==Patch changes==
* {{Patch 4.3.0|note=Added.}}

==See also==
* {{api|GetSpellCooldown}}
```