# API C SpellBook.GetSpellBookItemType

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Needs summary.
 itemType, actionID, spellID = C_SpellBook.GetSpellBookItemType(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}} - Spellbook slot index, ranging from 1 through the total number of spells across all tabs and pages
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;itemType:{{apitype|Enum.SpellBookItemType}}
{{:Enum.SpellBookItemType|nocaption=1}}
:;actionID:{{apitype|number}} - Represents a base spellID for spells, flyoutID for flyouts, or petActionID for pet actions
:;spellID:{{apitype|number?}} - May be nil if item is not a spell; Will be the overriding spellID if spell is overriden, otherwise will match actionID

==Details==
* New {{api|C_SpellBook.GetSpellBookItemInfo}} contains far more info than old {{api|GetSpellBookItemInfo}}
* {{api|C_SpellBook.GetSpellBookItemType}} is the direct replacement for just the type info that the old {{api|GetSpellBookItemInfo}} returned (+spellID as a new bonus 3rd return value)
```