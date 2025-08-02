# API C PetJournal.PickupPet

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 5.0.4}}
Places a battle pet onto the mouse cursor.
 C_PetJournal.PickupPet(petID)

==Arguments==
:;petID:{{apitype|string}} - GUID of a battle pet in your collection.

==Details==
* The function places a specific battle pet in your collection on your cursor.
* Battle pets on your cursor can be placed on your action bars.
* Attempting to pick up a battle pet that's already on the cursor clears the cursor instead.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|GetCursorInfo}}
```