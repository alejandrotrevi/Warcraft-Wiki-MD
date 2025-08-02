# API C PetJournal.GetOwnedBattlePetString

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a formatted string how many of a battle pet species the player has collected.
 ownedString = C_PetJournal.GetOwnedBattlePetString(speciesId)

==Arguments==
:;speciesId:{{apitype|number}} - Battle pet species ID.

==Returns==
:;ownedString:{{apitype|string}} - a description of how many pets of this species you've collected, e.g. "|cFFFFD200Collected (1/3)", or nil if you haven't collected any.

==Patch changes==
* {{Patch 5.1.0|note=Added.}}
```