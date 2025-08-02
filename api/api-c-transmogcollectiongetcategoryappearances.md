# API C TransmogCollection.GetCategoryAppearances

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns all appearances for a category. This is filtered by the [[Class_proficiencies|class proficiency]].
 appearances = C_TransmogCollection.GetCategoryAppearances(category [, transmogLocation])

==Arguments==
:;category:{{apitype|Enum.TransmogCollectionType}}
{{:Enum.TransmogCollectionType|nocaption=1}}
:;transmogLocation:{{apitype|TransmogLocation?}}

==Returns==
:;appearances:{{apitype|TransmogCategoryAppearanceInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|visualID}} || {{apitype|number}} || [[AppearanceID|Visual ID]]
|-
| {{apiname|isCollected}} || {{apitype|boolean}} || True if the visual has been collected
|-
| {{apiname|isFavorite}} || {{apitype|boolean}} || 
|-
| {{apiname|isHideVisual}} || {{apitype|boolean}} || True if the visual should be hidden, e.g. [[Hidden Helm]]
|-
| {{apiname|canDisplayOnPlayer}} || {{apitype|boolean}} || <font color="green">11.0.0</font>
|-
| {{apiname|uiOrder}} || {{apitype|number}} || 
|-
| {{apiname|exclusions}} || {{apitype|number}} || 
|-
| {{apiname|isUsable}} || {{apitype|boolean}} || 
|-
| {{apiname|hasRequiredHoliday}} || {{apitype|boolean}} || 
|-
| {{apiname|hasActiveRequiredHoliday}} || {{apitype|boolean}} || 
|-
| {{apiname|alwaysShowItem}} || {{apitype|boolean?}} || For internal testing only
|}

==Patch changes==
* {{Patch 11.1.7|note=Removed <code>restrictedSlotID</code> field in return value.}}
* {{Patch 9.2.5|note=Added <code>transmogLocation</code> argument.}}
* {{Patch 7.0.3|note=Added.}}
```