# API GetSpellHitModifier

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the amount of Spell Hit %, not from Spell Hit Rating, that your character has.
 hitMod = GetSpellHitModifier()

==Returns==
:;hitMod:{{apitype|number}} - hit modifier (e.g. 16 for 16%)

==Example==
Returns the Spell Hit Chance displayed in the paperdoll.<sup>[https://github.com/Gethe/wow-ui-source/blob/4.0.1a/FrameXML/PaperDollFrame.lua#L1616]</sup>
 /dump GetCombatRatingBonus(CR_HIT_SPELL) + GetSpellHitModifier();

==See also==
* {{api|GetHitModifier}}()
```