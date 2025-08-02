# API C PetJournal.IsPetSourceChecked

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the pet source is checked.
 isChecked = C_PetJournal.IsPetSourceChecked(index)

==Arguments==
:;index:{{apitype|number}} - Index (from 1 to GetNumPetSources()) of all available pet sources

==Returns==
:;isChecked:{{apitype|boolean}} - True if the source is checked, false if the source is unchecked

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|C_PetJournal.SetAllPetSourcesChecked}}
* {{api|C_PetJournal.SetPetSourceChecked}}
* {{api|C_PetJournal.GetNumPetSources}}
```