# API GetSpecializationRole

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Returns the role a specialization is intended to perform.
 roleToken = GetSpecializationRole(specIndex [, isInspect, isPet])

==Arguments==
:;specIndex:{{apitype|number}} - Specialization index, ascending from 1.
:;isInspect:{{apitype|boolean?}}
:;isPet:{{apitype|boolean?}}

==Returns==
:;roleToken:{{apitype|string}} - One of "DAMAGER", "TANK", "HEALER"; 0 if the query is invalid.

==Details==
* While the inspection/pet arguments are suggested by the syntax error message, the function only returns 0 when those arguments are used. FrameXML uses {{api|GetInspectSpecialization}}("unit") in conjunction with {{api|GetSpecializationRoleByID}}(id) instead.

==See also==
* {{api|GetNumSpecializations}}
* {{api|GetSpecializationInfo}}
* {{api|GetSpecializationRoleByID}}

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```