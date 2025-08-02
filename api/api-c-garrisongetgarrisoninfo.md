# API C Garrison.GetGarrisonInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information for your character's garrison.
 garrisonLevel, mapTexture, townHallX, townHallY = C_Garrison.GetGarrisonInfo(garrisonType)

==Arguments==
:;garrisonType:{{apitype|Enum.GarrisonType}}
{{:Enum.GarrisonType|nocaption=1}}

==Returns==
:;garrisonLevel:{{apitype|number?}}
:;mapTexture:{{apitype|string?}}
:;townHallX:{{apitype|number?}}
:;townHallY:{{apitype|number?}}

==Patch changes==
* {{Patch 7.0.3|note=garrisonType is now required, additional returns added.}}
* {{Patch 6.0.2|note=Added.}}
```