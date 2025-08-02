# API C PetJournal.PetIsTradable

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether or not a pet from the Pet Journal is tradable.
 isTradable = C_PetJournal.PetIsTradable(petID)

==Arguments==
:;petID:{{apitype|string}} - GUID of pet in Pet Journal (different than speciesID and displayID)

==Returns==
:;isTradable:{{apitype|boolean}}

==Details==
This is used by Blizzard to generate the red "Not Tradable" text on Pet Journal tooltips when false or nil.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See Also==
* {{api|C_PetJournal.PetIsCapturable}}
* {{api|C_PetJournal.PetCanBeReleased}}
```