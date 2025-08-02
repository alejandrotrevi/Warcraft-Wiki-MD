# API C TransmogCollection.GetAppearanceInfoBySource

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TransmogCollection|system=TransmogrifyCollection}}
Returns information about the appearance tied to the given sourceID
 info = C_TransmogCollection.GetAppearanceInfoBySource(itemModifiedAppearanceID)

==Arguments==
:;itemModifiedAppearanceID:{{apitype|number}} : [[SourceID]] - 2nd return value from {{api|C_TransmogCollection.GetItemInfo}}()

==Returns==
:;info:{{apitype|TransmogAppearanceInfoBySourceData}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|appearanceID}} || {{apitype|number}} || 
|-
| {{apiname|appearanceIsCollected}} || {{apitype|boolean}} || 
|-
| {{apiname|sourceIsCollected}} || {{apitype|boolean}} || 
|-
| {{apiname|sourceIsCollectedPermanent}} || {{apitype|boolean}} || 
|-
| {{apiname|sourceIsCollectedConditional}} || {{apitype|boolean}} || 
|-
| {{apiname|meetsTransmogPlayerCondition}} || {{apitype|boolean}} || 
|-
| {{apiname|appearanceHasAnyNonLevelRequirements}} || {{apitype|boolean}} || 
|-
| {{apiname|appearanceMeetsNonLevelRequirements}} || {{apitype|boolean}} || 
|-
| {{apiname|appearanceIsUsable}} || {{apitype|boolean}} || 
|-
| {{apiname|appearanceNumSources}} || {{apitype|number}} || Number of sources that have this appearanceID
|-
| {{apiname|sourceIsKnown}} || {{apitype|boolean}} || <font color="green">9.1.5</font>
|-
| {{apiname|canDisplayOnPlayer}} || {{apitype|boolean}} || <font color="green">11.0.0</font>
|-
| {{apiname|isAnySourceValidForPlayer}} || {{apitype|boolean}} || <font color="green">11.0.0</font>
|}

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```