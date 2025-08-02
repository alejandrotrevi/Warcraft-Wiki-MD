# API PetRename

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.7|removed=11.0.2}}
Renames your pet.
 PetRename(name)

==Arguments==
:;name:{{apitype|string}} - The new name of the pet

==Details==
: Only hunters and frost mages can rename their pets.
: Each pet can be renamed once. Using this function when the pet has already been renamed results in an error message.
```