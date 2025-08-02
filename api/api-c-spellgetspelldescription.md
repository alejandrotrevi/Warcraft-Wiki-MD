# API C Spell.GetSpellDescription

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns nil if spell is not found
 description = C_Spell.GetSpellDescription(spellIdentifier)

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}}

==Returns==
:;description:{{apitype|string}} - May be empty if spell's data isn't loaded yet; Listen for {{api|t=e|SPELL_TEXT_UPDATE}} event, or use [[SpellMixin]] to load asynchronously
```