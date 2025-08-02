# API GetNumSpecGroups

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of specialization group (dual specs) the player has.
 numSpecGroups = GetNumSpecGroups([b])

==Arguments==
:;b:{{apitype|boolean}} - In theory this returns information for the inspected target instead of the player. In practice, this seems to return 0 if true. Defaults to false.

==Returns==
:;numSpecGroups:{{apitype|number}} - number of available specialization groups; 1 for characters that have not learned dual-specializations, 2 for those that have. 

==Patch changes==
* {{Patch 5.0.4|note=Replaced {{api|GetNumTalentGroups}}.}}

==See also==
* {{api|GetActiveSpecGroup}}
* {{api|SetActiveSpecGroup}}
```