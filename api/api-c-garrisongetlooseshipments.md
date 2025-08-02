# API C Garrison.GetLooseShipments

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns Garrison shipments in progress.
 looseShipments = C_Garrison.GetLooseShipments(garrisonType)

==Arguments==
:;garrisonType:{{apitype|Enum.GarrisonType}}
{{:Enum.GarrisonType|nocaption=1}}

==Returns==
:;looseShipments:{{apitype|number[]}} - List of shipments. More information is available from {{api|C_Garrison.GetLandingPageShipmentInfoByContainerID}}.
```