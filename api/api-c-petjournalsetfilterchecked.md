# API C PetJournal.SetFilterChecked

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the filters in the filter menu.
 C_PetJournal.SetFilterChecked(filter, value)

==Arguments==
:;filter:{{apitype|number}} - Bitfield for each filter
:: LE_PET_JOURNAL_FILTER_COLLECTED: Pets you have collected
:: LE_PET_JOURNAL_FILTER_NOT_COLLECTED: Pets you have not collected
:;value:{{apitype|boolean}} - True to set the filter, false to clear the filter

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|C_PetJournal.IsFilterChecked}}
```