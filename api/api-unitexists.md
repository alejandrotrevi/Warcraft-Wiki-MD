# API UnitExists

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns true if the unit exists can be targeted.
 exists = UnitExists(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;exists:{{apitype|boolean}}

==Details==
* This API returns false for visible units that are unable to be targeted, such as inactive bosses on encounters like the [[Coven of Shivarra]]. For these cases, {{api|t=a|UnitIsVisible}} can be used instead.

==Example==
The snippet below prints a message describing what the player is targeting.
 if UnitExists("target") then
  print("You're targeting a " .. UnitName("target"))
 else
  print("You have no target")
 end
```