# API GetNumSpecializationsForClassID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|future=1|patch=11.0.5|link=https://github.com/Gethe/wow-ui-source/blob/11.0.5/Interface/AddOns/Blizzard_DeprecatedSpecialization/Deprecated_Specialization.lua#L9-L10}}
Returns the number of specializations available to a particular class.
 numSpecializations = GetNumSpecializationsForClassID(classID)

==Arguments==
:;classID:{{apitype|number}} : [[ClassId]]

==Returns==
:;numSpecializations:{{apitype|number}} - number of specializations available to characters of the specified class.

==Details==
* Druids currently have 4 available specializations, demon hunters have 2; other classes have 3.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

==See also==
* {{api|GetNumSpecializations}}
```