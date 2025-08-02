# API C PetBattles.GetNumPets

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of pets that the specified owner has in the pet battle.
 numPets = C_PetBattles.GetNumPets(petOwner)

==Arguments==
:;petOwner:{{apitype|number}}
{{:LE_BATTLE_PET_OWNERS|nocaption=1}}

==Returns==
:;numPets:{{apitype|number}} - Amount of pets that the current owner has in the pet battle (always 1-3).

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```