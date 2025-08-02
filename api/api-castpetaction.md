# API CastPetAction

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=The "pet" action type of [[SecureActionButtonTemplate]] can be used to call this function.}}
Cast the corresponding pet skill.
 CastPetAction(index[, target])

==Arguments==
:;index:{{apitype|number}} - pet action bar slot index, ascending from 1.
:;target:{{apitype|UnitToken?}} - The unit to cast the action on; defaults to "target".

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
```