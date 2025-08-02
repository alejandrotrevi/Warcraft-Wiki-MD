# API UnitInAnyGroup

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether or not the targeted unit is in a [[Group]] of any type. Instance, raid, party, etc.
 inGroup = UnitInAnyGroup(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit token of the unit to check group status for. Always returns false if no unit is provided.

==Returns==
:;inGroup:{{apitype|boolean}} - True if the target is in a group, false otherwise.
```