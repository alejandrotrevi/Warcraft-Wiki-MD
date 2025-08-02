# API GetTradeSkillNumMade

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Get the number of items made in each use of a tradeskill.
 minMade, maxMade = GetTradeSkillNumMade(skillId)

==Parameters==
===Arguments===
:(skillId)

:;skillId:{{apitype|number}} - Which tradeskill to query.
===Returns===
:minMade, maxMade

:;minMade:{{apitype|number}} - The minimum number of items that will be made.
:;maxMade:{{apitype|number}} - The maximum number of items that will be made.
```