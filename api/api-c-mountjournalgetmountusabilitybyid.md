# API C MountJournal.GetMountUsabilityByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns if a mount is currently usable by the player.
 isUsable, useError = C_MountJournal.GetMountUsabilityByID(mountID, checkIndoors)

==Arguments==
:;[[MountID|mountID]]:{{apitype|number}}
:;checkIndoors:{{apitype|boolean}}

==Returns==
:;isUsable:{{apitype|boolean}}
:;useError:{{apitype|string?}}

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```