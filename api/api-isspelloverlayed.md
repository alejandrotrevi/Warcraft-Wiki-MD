# API IsSpellOverlayed

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=11.2.0|link=https://github.com/Gethe/wow-ui-source/blob/11.2.0/Interface/AddOns/Blizzard_Deprecated/Deprecated_11_2_0.lua#L13-L15}}
Returns true if the specified spell currently has a proc / spell activation alert (glowing border).
 isTrue = IsSpellOverlayed(spellID)

==Arguments==
:;spellID:{{apitype|number}} - the spell ID number 

==Returns==
:;isTrue:{{apitype|boolean}} - is it true if the spell is already using SpellActivationAlert, false otherwise
```