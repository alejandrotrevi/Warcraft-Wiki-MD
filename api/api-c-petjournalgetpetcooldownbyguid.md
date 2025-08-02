# API C PetJournal.GetPetCooldownByGUID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the cooldown associated with summoning a battle pet companion.
 start, duration, isEnabled = C_PetJournal.GetPetCooldownByGUID(GUID)

==Arguments==
:;GUID:{{apitype|string}} - GUID of a battle pet in your collection to query the cooldown of.

==Returns==
:;start:{{apitype|number}} - the time the cooldown period began, based on {{api|GetTime}}().
:;duration:{{apitype|number}} - the duration of the cooldown period.
:;isEnabled:{{apitype|number}} - 1 if the cooldown is not paused.

==Details==
* If the queried pet is not currently on a cooldown, this function will return <code>0, 0, 1</code>.

==Patch changes==
* {{Patch 5.2.0|note=Added.}}
```