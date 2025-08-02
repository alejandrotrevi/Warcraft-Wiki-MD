# API C PetJournal.SetPetSourceChecked

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the pet source in the filter menu.
 C_PetJournal.SetPetSourceChecked(index, value)

==Arguments==
:;index:{{apitype|number}} - Index (from 1 to GetNumPetSources()) of all available pet sources
:;value:{{apitype|boolean}} - True to set the pet source, false to clear the pet source

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|C_PetJournal.SetAllPetSourcesChecked}}
* {{api|C_PetJournal.IsPetSourceChecked}}
* {{api|C_PetJournal.GetNumPetSources}}
```