# API C Spell.GetSpellPowerCost

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns a table containing one or more SpellPowerCostInfos, one for each power type this spell costs
 powerCosts = C_Spell.GetSpellPowerCost(spellIdentifier)

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}}

==Returns==
:;powerCosts:{{apitype|SpellPowerCostInfo[]?}} - May return nil if spell is not found or has no resource costs
{{:Struct SpellPowerCostInfo|nocaption=1}}
```