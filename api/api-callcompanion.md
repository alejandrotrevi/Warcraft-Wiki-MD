# API CallCompanion

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
{{Ambox
| image = [[Image:spell_holy_borrowedtime.png|48px]]
| border = red
| type = This API is deprecated in retail, see:
| info = - [[API C_PetJournal.SummonPetByGUID|C_PetJournal.SummonPetByGUID]]<br>- [[API C_MountJournal.SummonByID|C_MountJournal.SummonByID]]
}}
<!--desc-->Summons a companion.
 CallCompanion(type, id)

==Arguments==
:;type:{{apitype|string}} - The type of companion to summon or dismiss: "CRITTER" or "MOUNT".
:;id:{{apitype|number}} - The companion index to summon or dismiss, ascending from 1.

==Example==
The following macro summons the [alphabetically] first mount your character has acquired:
 /run CallCompanion("MOUNT",1)
The following macro summons a random mount your character has acquired:
 /run CallCompanion("MOUNT", random(GetNumCompanions("MOUNT")))

==Details==
* The list of companions is usually, but not always, alphabetically sorted. You may ''not'' rely on the indices to remain stable, even if the number of companions is not altered.

==Patch changes==
* {{Patch 5.0.3|note=Companions are now account-wide. This function only works for non-combat companions ([[battle pet]]s) your character had acquired before the account-wide merge, as well as ''all'' mounts. For summoning [[battle pet]]s, use the [[API #Pet_Journal_Functions|C_PetJournal]] API.}}
* {{Patch 3.0.2|note=Added.}}

==See also==
* {{api|GetNumCompanions}}
* {{api|GetCompanionInfo}}
```