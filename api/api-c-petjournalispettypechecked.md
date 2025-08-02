# API C PetJournal.IsPetTypeChecked

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the pet type is checked.
 isChecked = C_PetJournal.IsPetTypeChecked(index)

==Arguments==
:;index:{{apitype|number}} - Index (from 1 to GetNumPetTypes()) of all available pet types

==Returns==
:;isChecked:{{apitype|boolean}} - True if the filter is checked, false if the filter is unchecked

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|C_PetJournal.SetAllPetTypesChecked}}
* {{api|C_PetJournal.SetPetTypeFilter}}
* {{api|C_PetJournal.GetNumPetTypes}}
```