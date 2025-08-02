# API C PetJournal.PetIsCapturable

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether a battle pet in your collection is capturable (i.e. a wild pet).
 isCapturable = C_PetJournal.PetIsCapturable(petID)

==Arguments==
:;petID:{{apitype|string}} - GUID of a battle pet in your collection, e.g. "0x0000000000067932"

==Returns==
:;isCapturable:{{apitype|boolean}} - true if the pet can be captured through wild pet battles, false otherwise.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```