# API GetActionInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an action.
 actionType, id, subType = GetActionInfo(slot)

==Arguments==
:;slot:{{apitype|number}} - [[ActionSlot|Action slot]] to retrieve information about.

==Returns==
:;actionType:{{apitype|string}} - Type of action button. (e.g. spell, item, macro, companion, equipmentset, flyout)
:;id:{{apitype|number,string}} - Appropriate identifier for the action specified by actionType -- e.g. spell IDs for spells, item IDs for items, equipment set names for equipment sets.
:;subType:{{apitype|string}} - Additional identifier for the action specified by actionType -- e.g. whether the companion ID is for a MOUNT or a CRITTER companion.

==Example==
 local actionType, id, subType = GetActionInfo(1);
 if ( actionType =="companion" and subType== "MOUNT" ) then
 	print("Button 1 is a mount:", GetSpellLink(id))
 end
```