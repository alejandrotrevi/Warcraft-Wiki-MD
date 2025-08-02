# API CanBeRaidTarget

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the unit can be marked with a raid target icon.
 canBeRaidTarget = CanBeRaidTarget(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;canBeRaidTarget:{{apitype|boolean}} - true if raid target markers can be assigned to the queried unit, false otherwise.

==Patch changes==
* {{Patch 4.0.1|note=Added.}}

==See also==
* {{api|SetRaidTarget}}
```