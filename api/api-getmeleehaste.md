# API GetMeleeHaste

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the player's melee haste percentage.
 haste = GetMeleeHaste()

==Returns==
:;haste:{{apitype|number}}

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|GetCombatRating}}(CR_HASTE_MELEE)<br>{{api|GetCombatRatingBonus}}(CR_HASTE_MELEE) }}
|}

==Example==
<syntaxhighlight lang="lua">
/dump GetMeleeHaste()
</syntaxhighlight>
[[File:API_GetHaste_01.png]]
```