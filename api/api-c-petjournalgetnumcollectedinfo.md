# API C PetJournal.GetNumCollectedInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|n=API C_PetJournal.GetNumCollectedInfo}}
Returns the number of collected battle pets of a particular species.
 numCollected, limit = C_PetJournal.GetNumCollectedInfo(speciesId)

==Arguments==
:;speciesId:{{apitype|number}} - Battle pet species ID to query, e.g. 635 for Adder battle pets.

==Returns==
:;numCollected:{{apitype|number}} - Number of battle pets of the queried species the player has collected.
:;limit:{{apitype|number}} - Maximum number of battle pets of the queried species the player may collect.

==Patch changes==
* {{Patch 5.1.0|note=Added.}}
```