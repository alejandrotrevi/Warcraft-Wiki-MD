# API UnitIsGroupAssistant

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the unit is an assistant in your current group.
 isAssistant = UnitIsGroupAssistant(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;isAssistant:{{apitype|boolean}} - true if the unit is a raid assistant in your current group, false otherwise.

==Details==
* Group leaders and assistants can invite players to the group, set main tanks, world markers, etc.
* This function returns true only for players promoted to group assistants, either explicitly or via the "make everyone an assistant" option. It'll return false for the group leader.

==Patch changes==
* {{Patch 5.0.4|note=Replaced {{api|IsRaidOfficer}}, {{api|UnitIsRaidOfficer}}.}}

==See also==
* {{api|UnitIsGroupLeader}}
* {{api|IsEveryoneAssistant}}
```