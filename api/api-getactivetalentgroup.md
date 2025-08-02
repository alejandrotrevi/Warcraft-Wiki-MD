# API GetActiveTalentGroup

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index of the current active talent group.
 index = GetActiveTalentGroup(isInspect, isPet);

==Arguments==
;isInspect : Boolean - If true returns the information for the inspected unit instead of the player.
;isPet : Boolean - If true returns the information for the inspected pet.

==Returns==
;index : Number -  The index of the current active talent group (1 for primary / 2 for secondary).

==Patch changes==
* {{Patch 5.0.4|note=Replaced by {{api|GetActiveSpecGroup}}.}}
```