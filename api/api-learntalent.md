# API LearnTalent

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Learns the specified talent. 
 success = LearnTalent(talentID)

==Arguments==
:;talentID:{{apitype|number}}

==Returns==
:;success:{{apitype|boolean}} - Returns <code>false</code> when e.g. in combat.

==Example==
Learns holy priest's [[Trail of Light]] talent.
<syntaxhighlight lang="lua">
/run LearnTalent(19753)
</syntaxhighlight>

==See also==
* {{api|LearnPvpTalent}}()
```