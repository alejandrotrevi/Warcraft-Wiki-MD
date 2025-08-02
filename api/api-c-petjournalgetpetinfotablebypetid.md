# API C PetJournal.GetPetInfoTableByPetID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PetJournal|system=PetJournalInfo}}
Needs summary.
 info = C_PetJournal.GetPetInfoTableByPetID(petID)

==Arguments==
:;petID:{{apitype|string}}

==Returns==
:;info:{{apitype|PetJournalPetInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| speciesID || {{apitype|number}} || 
|-
| customName || {{apitype|string?}} || 
|-
| petLevel || {{apitype|number}} || 
|-
| xp || {{apitype|number}} || 
|-
| maxXP || {{apitype|number}} || 
|-
| displayID || {{apitype|number}} || 
|-
| isFavorite || {{apitype|boolean}} || 
|-
| icon || {{apitype|number}} || 
|-
| petType || {{apitype|number}} || 
|-
| creatureID || {{apitype|number}} || 
|-
| name || {{apitype|string?}} || 
|-
| sourceText || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| isWild || {{apitype|boolean}} || 
|-
| canBattle || {{apitype|boolean}} || 
|-
| tradable || {{apitype|boolean}} || 
|-
| unique || {{apitype|boolean}} || 
|-
| obtainable || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```