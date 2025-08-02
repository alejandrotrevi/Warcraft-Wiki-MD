# API GetSpellLevelLearned

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the respective level a spell is learned.
 level = GetSpellLevelLearned(spell)
       = GetSpellLevelLearned(index, bookType)

==Arguments==
{{:SpellArg}}

==Returns==
:;level:{{apitype|number}} - Returns <code>0</code> if there is no level requirement.

==Example==
Prints when the [[Levitate]] spell is learned.
<syntaxhighlight lang="lua">
/dump GetSpellLevelLearned(1706) -- 21
</syntaxhighlight>
```