# API UnitHonorLevel

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the current honor rank of the unit.
 honorLevel = UnitHonorLevel(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;honorLevel:{{apitype|number}} - The honor level of the unit. In [[Legion]] this resets to 1 every new Prestige level.

==See also==
* {{api|UnitHonor}}
* {{api|UnitHonorMax}}
```