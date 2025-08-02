# API C SpellBook.GetSpellBookItemCastCount

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns number of times a SpellBookItem can be cast, typically based on availability of things like required reagent items; Always returns 0 if item is not found or is not a spell
 castCount = C_SpellBook.GetSpellBookItemCastCount(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;castCount:{{apitype|number}}
```