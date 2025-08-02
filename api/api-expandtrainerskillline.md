# API ExpandTrainerSkillLine

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Expands a header in the trainer window, showing all spells below it.
 ExpandTrainerSkillLine(index)

==Arguments==
:;index:{{apitype|number}} - The index of a line in the trainer window (if the supplied index is not a header, an error is produced).
::Index 0 ("All") will expand all headers.
::Note that indices are affected by the trainer filter, see {{api|GetTrainerServiceTypeFilter}}() and {{api|SetTrainerServiceTypeFilter}}()

==Patch changes==
* {{Patch 4.0.1|note=Removed.}}

==See also==
* {{api|GetTrainerServiceInfo}}()
```