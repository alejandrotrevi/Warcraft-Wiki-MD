# API GetStablePetFoodTypes

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.7|removed=11.0.2}}
Returns the food types the specified stabled pet can eat.
 local PetFoodList = { GetStablePetFoodTypes(index) }

==Arguments==
:;index:{{apitype|number}} - The stable slot index of the pet: 0 for the current pet, 1 for the pet in the left slot, and 2 for the pet in the right slot.

==Returns==
:A list of the pet food type names, see [[API_GetPetFoodTypes|GetPetFoodTypes()]].

===Possible Food Type Names===
* Meat
* Fish
* Fruit
* Fungus
* Bread
* Cheese
```