# API C SpellBook.IsSpellBookItemPassive

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns true if the SpellBookItem is a passive spell; Will always return false if it is not a spell
 isPassive = C_SpellBook.IsSpellBookItemPassive(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;isPassive:{{apitype|boolean}}
```