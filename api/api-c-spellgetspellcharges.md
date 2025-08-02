# API C Spell.GetSpellCharges

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns a table of info about the charges of a charge-accumulating spell; May return nil if spell is not found or is not charge-based
 chargeInfo = C_Spell.GetSpellCharges(spellIdentifier)

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}}

==Returns==
:;chargeInfo:{{apitype|SpellChargeInfo}}
{{:Struct SpellChargeInfo|nocaption=1}}
```