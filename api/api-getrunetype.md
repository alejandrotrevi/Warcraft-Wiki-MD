# API GetRuneType

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets the type of rune for a given rune ID.
 runeType = GetRuneType(id)

== Parameters ==
<big>'''Arguments'''</big>

:;id : The rune's id. A number between 1 and 6 denoting which rune to be queried.

<big>'''Returns'''</big>

:;runeType - The type of rune that it is. 
:*1 : RUNETYPE_BLOOD
:*2 : RUNETYPE_CHROMATIC
:*3 : RUNETYPE_FROST
:*4 : RUNETYPE_DEATH

("CHROMATIC" refers to Unholy runes)
```