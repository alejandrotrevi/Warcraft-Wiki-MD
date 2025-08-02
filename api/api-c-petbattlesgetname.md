# API C PetBattles.GetName

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name(s) of a specific pet in the pet battle.
 customName, speciesName = C_PetBattles.GetName(petOwner, slot)

==Arguments==
:;petOwner:{{apitype|Enum.BattlePetOwner}}
{{:Enum.BattlePetOwner|nocaption=1}}
:;slot:{{apitype|number}} - Accepted values are 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.

==Returns==
:;customName:{{apitype|string}} - Name of the pet. If the pet has a custom name, it will be returned here. If not, it returns the species name here as well as in the second return.
:;speciesName:{{apitype|string}} - Name of the pet's Species.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```