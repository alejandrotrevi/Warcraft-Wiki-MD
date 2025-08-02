# API C SpellBook.GetSpellBookItemPowerCost

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns a table containing one or more SpellPowerCostInfos, one for each power type a SpellBookItem costs.
 powerCosts = C_SpellBook.GetSpellBookItemPowerCost(spellBookItemSlotIndex, spellBookItemSpellBank)

==Arguments==
:;spellBookItemSlotIndex:{{apitype|number}}
:;spellBookItemSpellBank:{{apitype|Enum.SpellBookSpellBank}}
{{:Enum.SpellBookSpellBank|nocaption=1}}

==Returns==
:;powerCosts:{{apitype|SpellPowerCostInfo[]?}} - May return nil if item is not found or has no resource costs
{{:Struct SpellPowerCostInfo|nocaption=1}}
```