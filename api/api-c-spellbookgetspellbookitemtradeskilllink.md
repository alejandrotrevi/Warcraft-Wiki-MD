# API C SpellBook.GetSpellBookItemTradeSkillLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns nil if SpellBookItem is not associated with a trade skill
 spellLink = C_SpellBook.GetSpellBookItemTradeSkillLink(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;spellLink:{{apitype|string}}
```