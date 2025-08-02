# API C MountJournal.SetIsFavorite

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MountJournal|system=MountJournal}}
Marks or unmarks the specified mount as a favorite.
 C_MountJournal.SetIsFavorite(mountIndex, isFavorite)

==Arguments==
:;mountIndex:{{apitype|number}} - Index of the mount, in the range of 1 to {{api|C_MountJournal.GetNumMounts}}() (inclusive)
:;isFavorite:{{apitype|boolean}}

==Details==
* Does nothing if the specified index is out of range.

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```