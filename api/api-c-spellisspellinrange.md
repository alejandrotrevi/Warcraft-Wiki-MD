# API C Spell.IsSpellInRange

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns true if the current target is within range of the spell; False if out of range; Nil if range check was invalid
 inRange = C_Spell.IsSpellInRange(spellIdentifier [, targetUnit])

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}}
:;targetUnit:{{apitype|UnitToken?}} - Optional specific target; If not supplied, player's current target (if any) will be used

==Returns==
:;inRange:{{apitype|boolean?}} - May be nil if the range check was invalid, ie due to unknown/invalid spell, missing/invalid target, etc
```