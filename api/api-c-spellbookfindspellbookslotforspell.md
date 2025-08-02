# API C SpellBook.FindSpellBookSlotForSpell

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
If found, returns the first slot position of a SpellBookItem matching the specified spell and criteria
 spellBookItemSlotIndex, spellBookItemSpellBank = C_SpellBook.FindSpellBookSlotForSpell(spellIdentifier [, includeHidden [, includeFlyouts [, includeFutureSpells [, includeOffSpec]]]])

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}}
:;includeHidden:{{apitype|boolean?|default=false}} - If true, search includes SpellBookItems that are hidden from the SpellBook UI (ex: spells that have been replaced, are also in a Flyout, etc)
:;includeFlyouts:{{apitype|boolean?|default=true}} - If true, search includes Flyout SpellBookItems containing the specified spell
:;includeFutureSpells:{{apitype|boolean?|default=false}} - If true, search includes SpellBookItems for spells that have not yet been learned
:;includeOffSpec:{{apitype|boolean?|default=false}} - If true, search includes SpellBookItems belonging to non-active specializations; If spell is in active and inactive spec, the active spec slot will always be returned

==Returns==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}
```