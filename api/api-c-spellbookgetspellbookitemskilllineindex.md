# API C SpellBook.GetSpellBookItemSkillLineIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Get the index of the SkillLine this SpellBookItem is part of
 skillLineIndex = C_SpellBook.GetSpellBookItemSkillLineIndex(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;skillLineIndex:{{apitype|number?}} - Will be nil if the specified SpellBookItem doesn't exist or isn't part of a SkillLine
```