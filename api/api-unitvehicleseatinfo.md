# API UnitVehicleSeatInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Needs summary.
 controlType, occupantName, serverName, ejectable, canSwitchSeats = UnitVehicleSeatInfo(unit, virtualSeatIndex)

==Arguments==
:;unit:{{apitype|UnitToken}}
:;virtualSeatIndex:{{apitype|number}}

==Returns==
:;controlType:{{apitype|string}}
:;occupantName:{{apitype|string}}
:;serverName:{{apitype|string}}
:;ejectable:{{apitype|boolean}}
:;canSwitchSeats:{{apitype|boolean}}
```