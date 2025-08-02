# API C Spell.GetOverrideSpell

**Contributor:** AlternativeTheory

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns the ID for the override spell.
 overrideSpellID = C_Spell.GetOverrideSpell(spellIdentifier [, spec [, onlyKnown [, ignoreOverrideSpellID]]])

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}}
:;spec:{{apitype|number?|default=0}} - Which Class Specialization to consider, as overrides may vary by Spec; Defaults to player's current Spec
:;onlyKnown:{{apitype|boolean?|default=true}}
:;ignoreOverrideSpellID:{{apitype|number?|default=0}}

==Returns==
:;overrideSpellID:{{apitype|number}} - Returns the spellID for the active version of the spell

==Details==
* Override spells replace a base spell; they are usually but not always gained via talents.
** For example, [[Gloomblade]] overrides (replaces) [[Backstab]] if you have selected the talent for it.
** Or [[Switch Flight Style]] which has a base version (only used before the first style switch on a char) and then two overrides depending on if you are in [[Flight Style: Steady]] or [[Flight Style: Skyriding]].
* The override spell returned is always the active override spell (this is slightly different behaviour to {{api|FindSpellOverrideByID}})
```