# API C SpellBook.IsSpellBookItemHelpful

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns true if the SpellBookIem can be cast on the player or other friendly targets
 isHelpful = C_SpellBook.IsSpellBookItemHelpful(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;isHelpful:{{apitype|boolean}}
```