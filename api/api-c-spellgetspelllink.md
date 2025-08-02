# API C Spell.GetSpellLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns the hyperlink for a spell.
 spellLink = C_Spell.GetSpellLink(spellIdentifier [, glyphID])

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}}
:;glyphID:{{apitype|number?}}

==Returns==
:;spellLink:{{apitype|string}} : [[Hyperlinks#spell|spellLink]] - Returns <code>nil</code> if spell is not found
```