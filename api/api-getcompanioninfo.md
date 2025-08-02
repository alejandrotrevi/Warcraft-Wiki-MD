# API GetCompanionInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
{{Ambox
| image = [[Image:spell_holy_borrowedtime.png|48px]]
| border = red
| type = This API is deprecated in retail, see:
| info = - [[API C_PetJournal.GetPetInfoByIndex|C_PetJournal.GetPetInfoByIndex]]<br>- [[API C_MountJournal.GetDisplayedMountInfo|C_MountJournal.GetDisplayedMountInfo]]
}}
<!--desc-->Returns info for a companion.
 creatureID, creatureName, creatureSpellID, icon, issummoned, mountType = GetCompanionInfo(type, id)

==Arguments==
:;type:{{apitype|string}} - Companion type to query: "CRITTER" or "MOUNT".
:;id:{{apitype|number}} - Index of the slot to query. Starting at 1 and going up to [[API GetNumCompanions|GetNumCompanions]]("type").

==Returns==
:;creatureID:{{apitype|number}} - The NPC ID of the companion.
:;creatureName:{{apitype|string}} - The name of the companion.
:;creatureSpellID:{{apitype|number}} - The spell ID to cast the companion.  This is not passed to {{api|CallCompanion}}, but can be used with, e.g., {{api|GetSpellInfo}}.
:;icon:{{apitype|string}} - The texture of the icon for the companion.
:;issummoned:{{apitype|boolean}} - 1 if the companion is summoned, nil if it's not.
:;mountType:{{apitype|number}} - Bitfield for air/ground/water mounts
:: 0x1: Ground 
:: 0x2: Can fly
:: 0x4: ? (set for most mounts)
:: 0x8: Underwater
:: 0x10: Can jump (turtles cannot)

==Details==
* The indices are ''unstable'': you may not rely on the <code>("type", id)</code> mapping to the same companion after an arbitrary amount of time, even if the player does not learn/unlearn any companions during the period.
* Generally, the indices are ordered alphabetically, though this order may be violated during the initial loading process and upon zoning.

==Patch changes==
* {{Patch 7.0.3|note=Deprecated (possibly earlier) in favor of {{api|C_MountJournal.GetMountInfoByID}}.}}
* {{Patch 5.0.3|note=Companions are now account-wide. This function only returns information about non-combat companions ([[battle pet]]s) your character had acquired before the account-wide merge, as well as ''all'' mounts. For information about [[battle pet]]s, use the [[API #Pet_Journal_Functions|C_PetJournal]] API.}}
* {{Patch 3.0.2|note=Added.}}

==See also==
* {{api|GetNumCompanions}}
* {{api|CallCompanion}}
* [[API #Pet_Journal_Functions|C_PetJournal function]]
```