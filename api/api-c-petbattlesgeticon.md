# API C PetBattles.GetIcon

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current icon of a specific pet in the pet battle.
 iconFileID = C_PetBattles.GetIcon(petOwner, slot)

==Arguments==
:;petOwner:{{apitype|Enum.BattlePetOwner}}
{{:Enum.BattlePetOwner|nocaption=1}}
:;slot:{{apitype|number}} - Accepted values are 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.

==Returns==
:;iconFileID:{{apitype|fileID}} - Full path of the species' icon

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```