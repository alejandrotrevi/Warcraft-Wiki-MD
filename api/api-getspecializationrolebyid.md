# API GetSpecializationRoleByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Returns the role a specialization is intended to perform.
 roleToken = GetSpecializationRoleByID(specID)

==Arguments==
:;specID:{{apitype|number}} - Specialization ID, as returned by {{api|GetSpecializationInfo}} or {{api|GetInspectSpecialization}}.

==Returns==
:;roleToken:{{apitype|string}} - One of "DAMAGER", "TANK", "HEALER"; nil if specID is invalid.

==See also==
* {{api|GetSpecializationRole}}

==Patch changes==
* {{Patch 5.0.4|note=Added.}}
```