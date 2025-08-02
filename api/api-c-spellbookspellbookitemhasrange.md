# API C SpellBook.SpellBookItemHasRange

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns true if the SpellBookIem has a min and/or max range greater than 0; Will always return false if it is not a spell
 hasRange = C_SpellBook.SpellBookItemHasRange(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;hasRange:{{apitype|boolean}}
```