# API C MountJournal.GetMountInfo

**Contributor:** Surafbrov

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the specified mount.
 creatureName, spellID, icon, active, isUsable, sourceType, isFavorite, isFactionSpecific, faction, hideOnChar, isCollected = C_MountJournal.GetMountInfo(index)

==Arguments==
; index : number - the index of the mount, in the range of 1 to {{api|C_MountJournal.GetNumMounts}}() (inclusive)

==Returns==
{| class="darktable zebra"
!Index!!Value!!Type!!Details
|-
|1||creatureName||String||The name of the mount
|-
|2||spellID||Number||The ID of the spell that summons the mount
|-
|3||icon||String||Path to the icon for the mount
|-
|4||active||Boolean||Indicates if the player is currently mounted on the mount
|-
|5||isUsable||Boolean||Indicates if the mount is usable based on the player's current location, riding skill, profession skill, class, etc.
|-
|6||sourceType||Number||Indicates generally how the mount may be obtained; see the 3rd return value from {{api|C_MountJournal.GetMountInfoExtra}} for specific information
|-
|7||isFavorite||Boolean||Indicates if the mount is currently marked as a favorite
|-
|8||isFactionSpecific||Boolean||true if the mount is only available to one faction, false otherwise
|-
|9||faction||Number/nil||0 if the mount is available only to Horde players, 1 if the mount is available only to Alliance players, or nil if the mount is not faction-specific
|-
|10||hideOnChar||Boolean||Indicates if the mount should be hidden in the player's mount journal (includes Swift Spectral Gryphon and mounts specific to the opposite faction)
|-
|11||isCollected||Boolean||Indicates if the player has learned the mount
|}

==Details==
Returns nothing if the specified index is out of bounds.

Current values of the <code>sourceType</code> return include:

* 0 - not categorized; includes many mounts that should (and may eventually) be included in one of the other categories
* 1 - Drop
* 2 - Quest
* 3 - Vendor
* 4 - Profession
* 5 - Pet Battle; currently includes only [[Felsteed]], which is learned by warlocks at level 20 and is probably mis-flagged
* 6 - Achievement
* 7 - World Event; currently includes only [[Swift Lovebird]]
* 8 - Promotion; currently includes only:
** [[Big Blizzard Bear]] from [[Blizzcon_2007|BlizzCon 2007]]
** [[Reins of the Dread Raven|Dread Raven]] from the [[World of Warcraft: Warlords of Draenor Collector's Edition|Warlords of Draenor Collector's Edition]]
** [[Hearthsteed]] from the [[Hearthstone (game)|Hearthstone]] release promotion
** [[Imperial Quilen]] from the [[World of Warcraft: Mists of Pandaria Collector's Edition|Mists of Pandaria Collector's Edition]]
** [[Ruby Panther]], which is crafted by Jewelcrafting and is probably mis-flagged
** [[Spectral Gryphon]] from the [[Scroll of Resurrection]] promotion
** [[Tyrael's Charger]] from the 2011‑2012 [[Annual Pass]] promotion
* 9 - [[TCG#Loot_Cards|Trading Card Game]]
* 10 - [[Shop items|Blizzard Pet Store]]

These are the same source type IDs and labels used in the pet journal.

==Patch changes==
* {{Patch 7.0.3|note=Replaced by {{api|C_MountJournal.GetDisplayedMountInfo}} and {{api|C_MountJournal.GetMountInfoByID}}.}}
* {{Patch 6.0.2|note=Added.}}

==See also==
* {{api|C_MountJournal.GetMountInfoExtra}}
```