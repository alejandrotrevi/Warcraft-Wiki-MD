# API C PetJournal.PetIsHurt

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the specified battle pet is injured and unable to participate in battles.
 isHurt = C_PetJournal.PetIsHurt(petID)

==Arguments==
:;petID:{{apitype|string}} - Battle pet GUID of a pet in your collection.

==Returns==
:;isHurt:{{apitype|boolean}} - true if the specified pet is injured and cannot fight, false otherwise.

==Details==
* Pets are injured by dying in pet battles, and may be cured by using [[Revive Battle Pets]], a [[Battle Pet Bandage]], or by visiting a [[Stable master]].

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```