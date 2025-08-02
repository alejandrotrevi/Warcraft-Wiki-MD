# API C MountJournal.GetIsFavorite

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MountJournal|system=MountJournal}}
Indicates whether the specified mount is marked as a favorite.
 isFavorite, canSetFavorite = C_MountJournal.GetIsFavorite(mountIndex)

==Arguments==
:;mountIndex:{{apitype|number}} - Index of the mount, in the range of 1 to {{api|C_MountJournal.GetNumMounts}}() (inclusive)

==Returns==
:;isFavorite:{{apitype|boolean}}
:;canSetFavorite:{{apitype|boolean}}

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```