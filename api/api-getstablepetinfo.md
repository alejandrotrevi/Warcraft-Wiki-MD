# API GetStablePetInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.7|removed=11.0.2}}
Returns info for a specific stabled pet.
 petIcon, petName, petLevel, petType, petTalents = GetStablePetInfo(index)

==Arguments==
:;index:{{apitype|number}} - The index of the pet slot, 1 through 5 are the hunter's active pets, 6 through 25 are the hunter's stabled pets.

==Returns==
:;petIcon:{{apitype|string}} - The path to texture to use as the icon for the pet, see [[API_GetPetIcon|GetPetIcon()]].
:;petName:{{apitype|string}} - The pet name, see [[API_UnitName|UnitName()]].
:;petLevel:{{apitype|number}} - The pet level, see [[API_UnitLevel|UnitLevel()]].
:;petType:{{apitype|string}} - The ''localized'' pet family, see [[API_UnitCreatureFamily|UnitCreatureFamily()]].
:;petTalents:{{apitype|string}} - The pet's [[Pet talents|talent group]].
```