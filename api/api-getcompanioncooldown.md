# API GetCompanionCooldown

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns cooldown information about the companions you have.
 startTime, duration, isEnabled = GetCompanionCooldown("type", id)

==Arguments==
;type : String ([[companionType]]) - Type of the companion being queried ("CRITTER" or "MOUNT")
;id : Number - The slot id to query (starts at 1).

==Returns==
;start : Number - the time the cooldown period began, based on {{api|GetTime}}().
;duration : Number - the duration of the cooldown period.
;isEnabled : Number - 1 if the companion has a cooldown.

==Patch changes==
* {{Patch 5.2.0|note={{api|C_PetJournal.GetPetCooldownByGUID}} added to return battle pet companion cooldown information.}}
* {{Patch 5.0.4|note=Removed.}}
* {{Patch 3.0.2|note=Added.}}
```