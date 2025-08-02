# API PickupAction

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.2}}
Places an action onto the cursor.
 PickupAction(slot)

==Arguments==
:;slot:{{apitype|number}} - The [[ActionSlot|action slot]] to pick the action up from.

==Details==
* If the slot is empty, nothing happens, otherwise the action from the slot is placed on the cursor, and the slot is filled with whatever action was currently being drag-and-dropped (The slot is emptied if the cursor was empty).
* If you wish to empty the cursor without putting the item into another slot, try [[API ClearCursor|ClearCursor]].
```