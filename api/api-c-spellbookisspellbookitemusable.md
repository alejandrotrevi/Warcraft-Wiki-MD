# API C SpellBook.IsSpellBookItemUsable

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns whether the SpellBookIem is currently castable.
 isUsable, insufficientPower = C_SpellBook.IsSpellBookItemUsable(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}} - Spellbook slot index, ranging from 1 through the total number of spells across all tabs and pages
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;isUsable:{{apitype|boolean}} - True if the spell is usable, false otherwise. A spell might be unusable for a variety of reasons, such as:
::* The player hasn't learned the spell
::* The player lacks required mana or reagents
::* Reactive conditions haven't been met
:;insufficientPower:{{apitype|boolean}} - True if spell is specifically unusable due to insufficient power (i.e., MANA, RAGE, etc)

==Patch changes==
* {{Patch 11.0.0|note=Added, replacement for {{api|IsUsableSpell}}.}}
```