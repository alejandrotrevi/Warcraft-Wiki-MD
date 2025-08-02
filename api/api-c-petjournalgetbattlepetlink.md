# API C PetJournal.GetBattlePetLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a battle pet link.
 link = C_PetJournal.GetBattlePetLink(petID)

==Arguments==
:;petID:{{apitype|string}} - GUID specifying a battle pet in your collection.

==Returns==
:;link:{{apitype|string}} - A chat link to the specified battle pet; nil if there is no pet with the specified petID in your collection.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```