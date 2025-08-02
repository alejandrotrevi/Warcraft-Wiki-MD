# API C PetBattles.GetBreedQuality

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the rarity of a specific pet in the current pet battle.
 quality = C_PetBattles.GetBreedQuality(petOwner, slot)

==Arguments==
:;petOwner:{{apitype|Enum.BattlePetOwner}}
{{:Enum.BattlePetOwner|nocaption=1}}
:;slot:{{apitype|number}} - Accepted values are 1-3, but the order is based off of the initial order. Which pet is currently active is irrelevant to the index, if it was your 3rd pet when you entered battle, it will always be 3 on the index.

==Returns==
:;quality:{{apitype|Enum.BattlePetBreedQuality}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || {{apiname|Poor}} || 
|-
| 1 || {{apiname|Common}} || 
|-
| 2 || {{apiname|Uncommon}} || 
|-
| 3 || {{apiname|Rare}} || 
|-
| 4 || {{apiname|Epic}} || 
|-
| 5 || {{apiname|Legendary}} || 
|}

==Details==
* Use <code>_G["BATTLE_PET_BREED_QUALITY"..rarity]</code> to convert the rarity to a String while drawing on Blizzard's pre-existing localization information.

==Patch changes==
* {{Patch 11.0.0|note=Changed return value to an enum|comment=The value was decremented by 1, it previously was <code>1: "Poor", 2: "Common", 3: "Uncommon", 4: "Rare", 5: "Epic", 6: "Legendary"</code>}}
* {{Patch 5.0.4|note=Added.}}
```