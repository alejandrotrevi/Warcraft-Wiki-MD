# API PickupCompanion

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 3.0.2}}
Places a mount onto the cursor.
 PickupCompanion(type, index)

==Arguments==
:;type:{{apitype|string}} - companion type, either "MOUNT" or "CRITTER".
:;index:{{apitype|number}} - index of the companion of the specified type to place on the cursor, ascending from 1.

==Details==
* You should only use this function to pick up ''mounts''; for critters, this function has been superseded by {{api|C_PetJournal.PickupPet}}, and instead places an unusable spell on the cursor.

==Patch changes==
* {{Patch 5.0.4|note="CRITTER" pick-up broken.}}
* {{Patch 3.0.2|note=Added.}}

==See also==
* {{api|GetCursorInfo}}
* {{api|GetCompanionInfo}}
* {{api|C_PetJournal.PickupPet}}
```