# API C TransmogCollection.GetAppearanceSourceInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns appearance info for a transmog source.
 categoryID, visualID, canEnchant, icon, isCollected, itemLink, transmogLink, unknown1, itemSubTypeIndex = C_TransmogCollection.GetAppearanceSourceInfo(sourceID)

==Arguments==
:;sourceID:{{apitype|number}}

==Returns==
:;categoryID:{{apitype|number}} : [[Enum.TransmogCollectionType]]
:;[[AppearanceID|visualID]]:{{apitype|number}}
:;canEnchant:{{apitype|boolean}}
:;icon:{{apitype|number}}
:;isCollected:{{apitype|boolean}} - notably, this works across class boundaries, unlike {{api|C_TransmogCollection.GetSourceInfo|GetSourceInfo}}() or {{api|C_TransmogCollection.GetAppearanceSources|GetAppearanceSources}}()
:;itemLink:{{apitype|string}}
:;transmogLink:{{apitype|string}} : [[Hyperlinks#transmogillusion|transmogillusionLink]]
:;unknown1:{{apitype|number}}
:;itemSubTypeIndex:{{apitype|number}} - Item's Index into the related [[ItemType|SubType Enum]]

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```