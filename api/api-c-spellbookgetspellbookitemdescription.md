# API C SpellBook.GetSpellBookItemDescription

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Needs summary.
 description = C_SpellBook.GetSpellBookItemDescription(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;description:{{apitype|string}} - May be empty if spell's data isn't loaded yet; Listen for SPELL_TEXT_UPDATE event, or use SpellMixin to load asynchronously
```