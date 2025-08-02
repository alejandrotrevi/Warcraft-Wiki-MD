# API C SpellBook.GetSpellBookItemCharges

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns a table of info about the charges of a charge-accumulating SpellBookItem; May return nil if item is not found or is not charge-based
 chargeInfo = C_SpellBook.GetSpellBookItemCharges(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;chargeInfo:{{apitype|SpellChargeInfo}}
{{:Struct SpellChargeInfo|nocaption=1}}
```