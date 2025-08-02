# API GetNumCompanions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
{{Ambox
| image = [[Image:spell_holy_borrowedtime.png|48px]]
| border = red
| type = This API is deprecated in retail, see:
| info = - [[API C_PetJournal.GetNumPets|C_PetJournal.GetNumPets]]<br>- [[API C_MountJournal.GetNumDisplayedMounts|C_MountJournal.GetNumDisplayedMounts]]
}}
<!--desc-->Returns the number of mounts.
 count = GetNumCompanions(type)

==Arguments==
:;type:{{apitype|string}} - Type of companions to count: "CRITTER", or "MOUNT".

==Returns==
:;count:{{apitype|number}} - The number of companions of a specific type.

==Example==
The following snippet prints how many mounts the player has collected.
 local count = GetNumCompanions("MOUNT");
 print('Hello, I have collected a total of ' .. count .. ' mounts.');

==Patch changes==
* {{Patch 5.0.4|note=Companions are now account-wide. This function only returns the correct value for mounts -- the non-combat companion count is based on the companions the character has acquired prior to the patch. Use the [[API #Pet_Journal_Functions|C_PetJournal]] API to query [[battle pet]]-related information.}}
* {{Patch 3.0.2|note=Added.}}
```