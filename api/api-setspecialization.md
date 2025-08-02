# API SetSpecialization

**Contributor:** Siiftun1857

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Selects a specialization.
 SetSpecialization(specIndex [, isPet])

==Arguments==
:;specIndex:{{apitype|number}} - Index of the specialization to select, ascending from 1.
:;isPet:{{apitype|boolean?}} - if true, set the select a specialization for the player's pet, otherwise, select a specialization for the player.

==Details==
* Starts changing specialization cast time regardless of given specIndex is valid or not.
* Fails if setting specialization to "Initial" with specIndex of 5.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|GetSpecializationInfo}}
```