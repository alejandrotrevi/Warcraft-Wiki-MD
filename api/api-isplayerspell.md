# API IsPlayerSpell

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|future=1|patch=11.2.0|link=https://github.com/Gethe/wow-ui-source/blob/11.2.0/Interface/AddOns/Blizzard_DeprecatedSpellBook/Deprecated_SpellBook.lua#L11-L14}}
Returns whether the player has learned a particular spell.
 isKnown = IsPlayerSpell(spellID)

==Arguments==
:;spellID:{{apitype|number}} - Spell ID of the spell to query, e.g. 1953 for [[Blink]].

==Returns==
:;isKnown:{{apitype|boolean}} - true if the player can cast this spell (or a different spell that overrides this spell), false otherwise.

==Details==
* Spells can be permanently or temporarily overridden by other spells as a result of procs, talents, or other spell mechanics, e.g.
** [[Moonfire]] is overriden by [[Sunfire]] while in [[Solar Eclipse]]
** [[Trap Launcher]] replaces trap spells by ranged variants
** [[Nether Tempest]] replaces a permanent base spell [[Mage Bomb]]
** [[Chakra]] replaces [[Holy Word: Chastise]] with different spells
* Querying the base (replaced) spell will also return true if any of its overrides are currently active.
* Querying an overriding spell may or may not return true even if that spell is currently known, depending on the particular spell.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|GetSpellInfo}}
```