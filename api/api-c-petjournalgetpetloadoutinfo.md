# API C PetJournal.GetPetLoadOutInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a slot in your battle pet team.
 petGUID, ability1, ability2, ability3, locked = C_PetJournal.GetPetLoadOutInfo(slotIndex)

==Arguments==
:;slotIndex:{{apitype|number}} - battle pet slot index, an integer between 1 and 3. Values outside this range throw an error.

==Returns==
:;petGUID:{{apitype|string}} - GUID of the battle pet currently in this slot.
:;ability1:{{apitype|number}} - Ability ID of the first (level 1/10) ability selected for the battle pet in this slot.
:;ability2:{{apitype|number}} - Ability ID of the second (level 2/15) ability selected for the battle pet in this slot.
:;ability3:{{apitype|number}} - Ability ID of the third (level 4/20) ability selected for the battle pet in this slot.
:;locked:{{apitype|boolean}} - false if the player can place a battle pet in this slot, true otherwise.

==Details==
* Ability IDs are returned even for slots that are not yet unlocked by a low-level battle pet.
* Slots are locked until the player has earned the necessary achievement/skill. The first slot is unlocked by learning [[Battle Pet Training]].

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```