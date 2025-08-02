# API C TransmogCollection.GetAppearanceSources

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TransmogCollection|system=TransmogrifyCollection}}
Returns the sources for an appearance.
 sources = C_TransmogCollection.GetAppearanceSources(appearanceID [, categoryType, transmogLocation])

==Arguments==
:;appearanceID:{{apitype|number}} : [[AppearanceID]]
:;categoryType:{{apitype|Enum.TransmogCollectionType?|link=1}}
:;transmogLocation:{{apitype|TransmogLocationMixin?}}

==Returns==
:;sources:{{apitype|AppearanceSourceInfo[]?}} - Only returns valid data for the [[Class_proficiencies|class proficiency]], otherwise returns nil.
{{:Struct AppearanceSourceInfo|nocaption=1}}

==Details==
* This returns only known appearance sources, while {{api|C_TransmogCollection.GetAllAppearanceSources}} returns all appearance sources.

==Patch changes==
* {{Patch 9.2.5|note=Added <code>transmogLocation</code> argument.}}
* {{Patch 9.1.5|note=Added <code>categoryType</code> argument.}}
* {{Patch 9.1.0|note=Removed <code>categoryID</code> argument.}}
* {{Patch 9.0.1|note=Added <code>categoryID</code> argument.}}
* {{Patch 7.0.3|note=Added.}}
```