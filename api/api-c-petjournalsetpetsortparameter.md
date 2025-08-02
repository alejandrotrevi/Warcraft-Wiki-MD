# API C PetJournal.SetPetSortParameter

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Changes the battle pet ordering in the pet journal.
 C_PetJournal.SetPetSortParameter(sortParameter)

==Arguments==
:;sortParameter:{{apitype|number}} - Index of the ordering type that should be applied to {{api|C_PetJournal.GetPetInfoByIndex}} returns; one of the following global numeric values:
::*LE_SORT_BY_NAME
::*LE_SORT_BY_LEVEL
::*LE_SORT_BY_RARITY
::*LE_SORT_BY_PETTYPE

==Patch changes==
* {{Patch 5.1.0|note=Added.}}

==See also==
* {{api|C_PetJournal.GetPetSortParameter}}
```