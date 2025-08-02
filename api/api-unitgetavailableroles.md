# API UnitGetAvailableRoles

**Contributor:** DokoNinjaroboto

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the recommended roles for a specified unit
 tank, heal, dps = UnitGetAvailableRoles(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;tank:{{apitype|boolean}} - Whether the unit can perform as a tank
:;heal:{{apitype|boolean}} - Whether the unit can perform as a healer
:;dps:{{apitype|boolean}} - Whether the unit can perform as a dps

==Notes==
Although the Group Finder allows every class to pick any role, for some there is a warning that it is not recommended (e.g., healer as a Warrior). This function returns results based on the same logic.
```