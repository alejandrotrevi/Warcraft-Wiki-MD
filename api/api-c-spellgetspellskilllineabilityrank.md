# API C Spell.GetSpellSkillLineAbilityRank

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Spell|system=Spell}}
Returns the rank of a spell that corresponds to an ability within a ranked SkillLine (ex: a crafting Recipe); Returns nil if spell is not found, or isn't part of a ranked SkillLine
 rank = C_Spell.GetSpellSkillLineAbilityRank(spellIdentifier)

==Arguments==
:;spellIdentifier:{{apitype|SpellIdentifier}}

==Returns==
:;rank:{{apitype|number}}
```