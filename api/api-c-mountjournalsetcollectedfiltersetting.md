# API C MountJournal.SetCollectedFilterSetting

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MountJournal|system=MountJournal}}
Enables or disables the specified mount journal filter.
 C_MountJournal.SetCollectedFilterSetting(filterIndex, isChecked)

==Arguments==
:;filterIndex:{{apitype|number}}
{{:LE_MOUNT_JOURNAL_FILTER|nocaption=1}}
:;isChecked:{{apitype|boolean}}

==Details==
* Does nothing if the specified ID is not associated with an existing filter.

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```