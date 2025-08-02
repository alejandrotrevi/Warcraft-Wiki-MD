# API UnitIsTrivial

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns true if the unit is trivial (i.e. "grey" to the player).
 isTrivial = UnitIsTrivial(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;isTrivial:{{apitype|boolean}} - True if the unit is comparatively too low level to provide experience or honor; otherwise false.

==Details==
* At level 60, units level 47 and under are trivial.{{fact}} <!-- this was written in 2008 -->
* Trivial units continue to give loot, quest credit and (reduced) faction rep.
```