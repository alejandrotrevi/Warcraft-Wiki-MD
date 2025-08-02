# API GetSpellDescription

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=11.0.0|removed=11.0.2}}
Returns the spell description.
 desc = GetSpellDescription(spellID)

==Arguments==
:;spellID:{{apitype|number}} - Not readily available on function call, see [[SpellMixin#ContinueOnSpellLoad|SpellMixin:ContinueOnSpellLoad]].

==Returns==
:;desc:{{apitype|string}}

==Example==
 GetSpellDescription([https://www.wowhead.com/spell=11366/pyroblast 11366])

 > "Hurls an immense fiery boulder that causes 141 Fire damage."

==Patch changes==
* {{Patch 4.0.1|note=Added.}}
```