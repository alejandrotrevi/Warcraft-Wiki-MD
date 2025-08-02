# API C PetJournal.SetPetTypeFilter

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the pet type in the filter menu.
 C_PetJournal.SetPetTypeFilter(index, value)

==Arguments==
:;index:{{apitype|number}} - Index (from 1 to GetNumPetTypes()) of all available pet types
:;value:{{apitype|boolean}} - True to set the pet type, false to clear the pet type

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|C_PetJournal.SetAllPetTypesChecked}}
* {{api|C_PetJournal.IsPetTypeChecked}}
* {{api|C_PetJournal.GetNumPetTypes}}
```