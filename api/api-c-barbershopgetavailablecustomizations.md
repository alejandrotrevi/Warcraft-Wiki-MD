# API C BarberShop.GetAvailableCustomizations

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_BarberShop|system=BarberShop}}
Needs summary.
 categories = C_BarberShop.GetAvailableCustomizations()

==Returns==
:;categories:{{apitype|CharCustomizationCategory[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| id || {{apitype|number}} || 
|-
| orderIndex || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| icon || {{apitype|textureAtlas}} || 
|-
| selectedIcon || {{apitype|textureAtlas}} || 
|-
| undressModel || {{apitype|boolean}} || 
|-
| subcategory || {{apitype|boolean}} || 
|-
| cameraZoomLevel || {{apitype|number}} || 
|-
| cameraDistanceOffset || {{apitype|number}} || 
|-
| spellShapeshiftFormID || {{apitype|number?}} || 
|-
| chrModelID || {{apitype|number?}} || 
|-
| options || {{apitype|CharCustomizationOption[]}} || 
|-
| hasNewChoices || {{apitype|boolean}} || 
|-
| needsNativeFormCategory || {{apitype|boolean}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ CharCustomizationOption
! Field !! Type !! Description
|-
| id || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| orderIndex || {{apitype|number}} || 
|-
| optionType || {{apitype|Enum.ChrCustomizationOptionType}} || 
|-
| choices || {{apitype|CharCustomizationChoice[]}} || 
|-
| currentChoiceIndex || {{apitype|number?}} || 
|-
| hasNewChoices || {{apitype|boolean}} || 
|-
| isSound || {{apitype|boolean}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.ChrCustomizationOptionType
! Value !! Field !! Description
|-
| 0 || {{apiname|Dropdown}} || <font color="green">11.0.0</font> - Renamed from <code>SelectionPopout</code>
|-
| 1 || {{apiname|Checkbox}} || 
|-
| 2 || {{apiname|Slider}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ CharCustomizationChoice
! Field !! Type !! Description
|-
| id || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| ineligibleChoice || {{apitype|boolean}} || 
|-
| isNew || {{apitype|boolean}} || <font color="green">9.1.5</font>
|-
| swatchColor1 || {{apitype|colorRGB?}} || 
|-
| swatchColor2 || {{apitype|colorRGB?}} || 
|-
| soundKit || {{apitype|number?}} || <font color="green">10.1.0</font>
|-
| isLocked || {{apitype|boolean}} || <font color="green">10.0.2</font>
|-
| lockedText || {{apitype|string?}} || <font color="green">10.0.2</font>
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```