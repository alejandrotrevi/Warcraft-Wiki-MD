# API PickupPetAction

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.2}}
Places a pet action onto the cursor.
 PickupPetAction(petActionSlot)

==Arguments==
:;petActionSlot:{{apitype|number}} - The pet action slot to pick the action up from (1-10).

==Details==
* If the slot is empty, nothing happens, otherwise the action from the slot is placed on the cursor, and the slot is filled with whatever action was currently being drag-and-dropped (The slot is emptied if the cursor was empty).
```