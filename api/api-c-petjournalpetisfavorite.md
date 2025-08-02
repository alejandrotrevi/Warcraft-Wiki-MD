# API C PetJournal.PetIsFavorite

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the collected battle pet is favorited.
 isFavorite = C_PetJournal.PetIsFavorite(petGUID)

==Arguments==
:;petGUID:{{apitype|string}} - GUID of a battle pet in your collection.

==Returns==
:;isFavorite:{{apitype|boolean}} - true if this pet is marked as a favorite, false otherwise.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```