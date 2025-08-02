# API UnitInRaid

**Contributor:** Kanegasi

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index if the unit is in your raid group.
 index = UnitInRaid(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;index:{{apitype|number}} - same number in the raid## UnitId, feed into {{api|GetRaidRosterInfo}}

==Details==
* Pets are not considered to be part of your raid group.

==See also==
* {{api|UnitInParty}}()
```