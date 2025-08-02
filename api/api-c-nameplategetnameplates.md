# API C NamePlate.GetNamePlates

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the currently visible nameplates.
 nameplates = C_NamePlate.GetNamePlates([isSecure])

==Arguments==
:;isSecure:{{apitype|boolean?}} - Whether protected nameplates for friendly units while in instanced areas should be returned.

==Returns==
:;nameplates:{{apitype|Nameplate[]}} : {{api|t=o|Frame}}|[https://github.com/Gethe/wow-ui-source/blob/10.2.0/Interface/AddOns/Blizzard_NamePlates/Blizzard_NamePlates.lua#L540 NamePlateBaseMixin]
{{:API_C_NamePlate.GetNamePlateForUnit}}
```