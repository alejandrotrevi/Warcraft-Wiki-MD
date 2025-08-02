# API UnitPlayerOrPetInRaid

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if a different unit or pet is a member of the raid.
 inRaid = UnitPlayerOrPetInRaid(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;inRaid:{{apitype|boolean}}

==Details==
* Returns nil for player and pet as of 3.0.2

==Example==
 local TargetInRaid = UnitPlayerOrPetInRaid("target")

====Result====
 TargetInRaid = 1   - If your target is in your raid group.
 TargetInRaid = nil - If your target is not in raid group.
```