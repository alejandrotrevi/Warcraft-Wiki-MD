# API UnitSetRole

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Sets a unit's role in the group.
 result = UnitSetRole(unit [, roleStr])

==Arguments==
:;unit:{{apitype|UnitToken}}
:;roleStr:{{apitype|string?}} : <code>["TANK", "HEALER", "DAMAGER", "NONE"]</code>

==Returns==
:;result:{{apitype|boolean}}

==Details==
* It's not possible to assign roles to classes that are not capable of fulfilling that role.
```