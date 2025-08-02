# API C SpellBook.GetCurrentLevelSpells

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SpellBook|system=SpellBook}}
Returns general, class, and active spec spells that are learned at the specified level.
 spellIDs = C_SpellBook.GetCurrentLevelSpells(level)

==Arguments==
:;level:{{apitype|number}}

==Returns==
:;spellIDs:{{apitype|number[]}}

==Example==
<syntaxhighlight lang="lua">
/dump C_SpellBook.GetCurrentLevelSpells(2)
>> {589} -- Shadow Word: Pain
</syntaxhighlight>

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```