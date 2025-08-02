# API PlaceAction

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Places an action onto into the specified action slot.
 PlaceAction(slot)

==Arguments==
:;slot:{{apitype|number}} - The action slot to place the action into.

==Details==
* If the cursor is empty, nothing happens, otherwise the action from the cursor is placed in the slot. If the slot was empty then the cursor becomes empty, otherwise the action from the slot is picked up and placed onto the cursor.
* If an action is placed on the cursor use [[API_PutItemInBackpack]] to remove the action from the cursor without placing it in an action slot
* IMPORTANT: You can crash your client if you send an invalid slot number.
```