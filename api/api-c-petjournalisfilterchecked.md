# API C PetJournal.IsFilterChecked

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the selected filter is checked.
 isFiltered = C_PetJournal.IsFilterChecked(filter)

==Arguments==
:;filter:{{apitype|number}} - Bitfield for each filter
:: LE_PET_JOURNAL_FILTER_COLLECTED: Pets you have collected
:: LE_PET_JOURNAL_FILTER_NOT_COLLECTED: Pets you have not collected

==Returns==
:;isFiltered:{{apitype|boolean}} - True if the filter is checked, false if the filter is unchecked

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|C_PetJournal.SetFilterChecked}}
```