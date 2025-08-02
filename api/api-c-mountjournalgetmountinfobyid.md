# API C MountJournal.GetMountInfoByID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MountJournal|system=MountJournal}}
Returns information about the specified mount.
 name, spellID, icon, isActive, isUsable, sourceType, isFavorite, isFactionSpecific, faction, shouldHideOnChar, isCollected, mountID, isSteadyFlight
     = C_MountJournal.GetMountInfoByID(mountID)
     = C_MountJournal.GetDisplayedMountInfo(displayIndex)

==Arguments==
===<font color="#4ec9b0">GetMountInfoByID</font>===
:;mountID:{{apitype|number}} : [[MountID]] - Returned from {{api|C_MountJournal.GetMountIDs}}()

===<font color="#4ec9b0">GetDisplayedMountInfo</font>===
:;displayIndex:{{apitype|number}} - Index of the displayed mount in the mount journal list with the current search query and filters. Ranging from 1 to {{api|C_MountJournal.GetNumDisplayedMounts}}()

==Returns==
:;1. name:{{apitype|string}} - The name of the mount.
:;2. spellID:{{apitype|number}} - The ID of the spell that summons the mount.
:;3. icon:{{apitype|number}} : [[FileID]] - Icon texture used by the mount.
:;4. isActive:{{apitype|boolean}} - Indicates if the player is currently mounted on the mount.
:;5. isUsable:{{apitype|boolean}} - Indicates if the mount is usable based on the player's current location, riding skill, profession skill, class, etc.
:;6. sourceType:{{apitype|number}} - Indicates generally how the mount may be obtained; a localized string describing the acquisition method is returned by {{api|C_MountJournal.GetMountInfoExtraByID}}.
:;7. isFavorite:{{apitype|boolean}} - Indicates if the mount is currently marked as a favorite.
:;8. isFactionSpecific:{{apitype|boolean}} - true if the mount is only available to one faction, false otherwise.
:;9. faction:{{apitype|Enum.PvPFaction?}} - 0 if the mount is available only to Horde players, 1 if the mount is available only to Alliance players, or nil if the mount is not faction-specific.
{{:Enum.PvPFaction|nocaption=1}}
:;10. shouldHideOnChar:{{apitype|boolean}} - Indicates if the mount should be hidden in the player's mount journal (includes Swift Spectral Gryphon and mounts specific to the opposite faction).
:;11. isCollected:{{apitype|boolean}} - Indicates if the player has learned the mount.
:;12. mountID:{{apitype|number}} - ID of the mount.
:;13. isSteadyFlight:{{apitype|boolean}} - true if mount supports only steady flight.

==Details==
Current values of the <code>sourceType</code> return include:
* 0 - not categorized; includes many mounts that should (and may eventually) be included in one of the other categories
{{:Const_BATTLE_PET_SOURCE}}

==Patch changes==
* {{Patch 11.0.0|note=<code>isForDragonriding</code> replaced with <code>isSteadyFlight</code> return.}}
* {{Patch 10.0.0|note=Added <code>isForDragonriding</code> return.}}
* {{Patch 7.0.3|note=Added. Replaces {{api|C_MountJournal.GetMountInfo}}()}}
```