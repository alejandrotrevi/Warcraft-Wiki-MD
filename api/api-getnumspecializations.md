# API GetNumSpecializations

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of available specializations.
 numSpecializations = GetNumSpecializations([isInspect, isPet])

==Arguments==
:;isInspect:{{apitype|boolean?}} - if true, return information for the inspected unit; false by default
:;isPet:{{apitype|boolean?}} - if true, return information for the player's pet; false by default
If both arguments are false, the function returns information concerning the player.

==Returns==
:;numSpecializations:{{apitype|number}} - number of available specializations.

==Details==
{| {{apitable}}
{{apirow | Related API | {{api|GetNumSpecializationsForClassID}} }}
|}

==Patch changes==
* {{Patch 5.0.4|note=Replaced {{api|GetNumTalentTabs}}.}}
```