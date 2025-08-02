# API UnitGroupRolesAssigned

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns the assigned role for players in your group or raid.
  role = UnitGroupRolesAssigned(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;role:{{apitype|string}} - TANK, HEALER, DAMAGER, NONE

==See Also==
* {{api|t=e|PLAYER_ROLES_ASSIGNED}} happens whenever a group/raid member's roles are changed
* {{api|t=e|ROLE_CHANGED_INFORM}} also happens whenever a group/raid member's roles are changed, who changed it, from what, to what. Drives the chat message
```