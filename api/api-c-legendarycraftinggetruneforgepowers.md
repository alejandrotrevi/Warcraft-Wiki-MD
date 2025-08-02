# API C LegendaryCrafting.GetRuneforgePowers

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LegendaryCrafting|system=LegendaryCrafting}}
Needs summary.
 primaryRuneforgePowerIDs, otherRuneforgePowerIDs = C_LegendaryCrafting.GetRuneforgePowers([baseItem, filter])

==Arguments==
:;baseItem:{{apitype|ItemLocationMixin?}}
:;filter:{{apitype|Enum.RuneforgePowerFilter?}}
{{:Enum.RuneforgePowerFilter|nocaption=1}}

==Returns==
:;primaryRuneforgePowerIDs:{{apitype|number[]}}
:;otherRuneforgePowerIDs:{{apitype|number[]}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```