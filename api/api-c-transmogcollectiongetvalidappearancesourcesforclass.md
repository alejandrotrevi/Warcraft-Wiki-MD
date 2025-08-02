# API C TransmogCollection.GetValidAppearanceSourcesForClass

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TransmogCollection|system=TransmogrifyCollection}}
Needs summary.
 sources = C_TransmogCollection.GetValidAppearanceSourcesForClass(appearanceID, classID [, categoryType, transmogLocation])

==Arguments==
:;appearanceID:{{apitype|number}}
:;classID:{{apitype|number}}
:;categoryType:{{apitype|Enum.TransmogCollectionType?}}
{{:Enum.TransmogCollectionType|nocaption=1}}
:;transmogLocation:{{apitype|TransmogLocation?}}

==Returns==
:;sources:{{apitype|AppearanceSourceInfo[]}}
{{:Struct AppearanceSourceInfo|nocaption=1}}
```