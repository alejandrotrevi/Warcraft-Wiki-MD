# API GetEffectivePlayerMaxLevel

**Contributor:** Bigsxy

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the effective level cap for the current player
 effectiveMaxLevel = GetEffectivePlayerMaxLevel()

==Returns==
:;effectiveMaxLevel:{{apitype|number}} - The max level the currently logged in player can attain.

==Details==
* return value can be different from [[API GetMaxPlayerLevel|GetMaxPlayerLevel]] and [[API GetMaxLevelForExpansionLevel|GetMaxLevelForExpansionLevel]] depending on a users subscription status or if playing on a windowed level cap servers as seen in [[World of Warcraft Classic: Season of Discovery|Season of Discovery]].
```