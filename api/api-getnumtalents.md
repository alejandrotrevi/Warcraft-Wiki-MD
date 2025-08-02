# API GetNumTalents

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the amount of talents for a specialization.
 numTalents = GetNumTalents(tabIndex)

==Arguments==
:;tabIndex:{{apitype|number}} - Ranging from 1 to {{api|GetNumTalentTabs}}()

==Returns==
:;numTalents:{{apitype|number}} - The amount of talents offered by a specialization.

==Patch changes==
* {{Patch 6.0.2|note=Removed.}}

==See also==
* {{api|UnitCharacterPoints}} - returns the amount of unspent talent points
* {{Wow-inline}} {{api|GetTalentInfo/Classic}}
```