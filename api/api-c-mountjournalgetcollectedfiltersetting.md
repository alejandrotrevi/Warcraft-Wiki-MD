# API C MountJournal.GetCollectedFilterSetting

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MountJournal|system=MountJournal}}
Indicates whether the specified mount journal filter is enabled.
 isChecked = C_MountJournal.GetCollectedFilterSetting(filterIndex)

==Arguments==
:;filterIndex:{{apitype|number}}
{{:LE_MOUNT_JOURNAL_FILTER|nocaption=1}}

==Returns==
:;isChecked:{{apitype|boolean}} - true if the filter is enabled (mounts matching the filter are displayed), or false if the filter is disabled (mounts matching the filter are hidden)

==Details==
* Returns <code>true</code> if the specified ID is not associated with an existing filter.

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```