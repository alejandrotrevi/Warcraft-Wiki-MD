# API C UIWidgetManager.GetTextureAndTextRowVisualizationInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetTextureAndTextRowVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|TextureAndTextRowVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|shownState}} || {{apitype|Enum.WidgetShownState}} || 
|-
| {{apiname|entries}} || {{apitype|TextureAndTextEntryInfo[]}} || 
|-
| {{apiname|textSizeType}} || {{apitype|Enum.UIWidgetTextureAndTextSizeType}} || 
|-
| {{apiname|groupAlignment}} || {{apitype|Enum.UIWidgetHorizontalDirection}} || <font color="green">11.0.0</font>
|-
| {{apiname|fixedWidth}} || {{apitype|number?}} || 
|-
| {{apiname|tooltipLoc}} || {{apitype|Enum.UIWidgetTooltipLocation}} || 
|-
| {{apiname|widgetSizeSetting}} || {{apitype|number}} || 
|-
| {{apiname|textureKit}} || {{apitype|textureKit}} || 
|-
| {{apiname|frameTextureKit}} || {{apitype|textureKit}} || 
|-
| {{apiname|hasTimer}} || {{apitype|boolean}} || 
|-
| {{apiname|orderIndex}} || {{apitype|number}} || 
|-
| {{apiname|widgetTag}} || {{apitype|string}} || 
|-
| {{apiname|inAnimType}} || {{apitype|Enum.WidgetAnimationType}} || 
|-
| {{apiname|outAnimType}} || {{apitype|Enum.WidgetAnimationType}} || 
|-
| {{apiname|widgetScale}} || {{apitype|Enum.UIWidgetScale}} || 
|-
| {{apiname|layoutDirection}} || {{apitype|Enum.UIWidgetLayoutDirection}} || 
|-
| {{apiname|modelSceneLayer}} || {{apitype|Enum.UIWidgetModelSceneLayer}} || 
|-
| {{apiname|scriptedAnimationEffectID}} || {{apitype|number}} || 
|}

{{:Enum.WidgetShownState}}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ TextureAndTextEntryInfo
! Field !! Type !! Description
|-
| {{apiname|text}} || {{apitype|string}} || 
|-
| {{apiname|tooltip}} || {{apitype|string}} || 
|}

{{:Enum.UIWidgetTextureAndTextSizeType}}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.UIWidgetHorizontalDirection
! Value !! Field !! Description
|-
| 0 || {{apiname|LeftToRight}} || 
|-
| 1 || {{apiname|RightToLeft}} || 
|}

{{:Enum.UIWidgetTooltipLocation}}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}

==Patch changes==
* {{Patch 10.0.2|note=Changed <code>textSizeType</code> field from <code>UIWidgetTextSizeType</code> to <code>UIWidgetTextureAndTextSizeType</code>.}}
* {{Patch 10.0.0|note=Added <code>fixedWidth</code> field.}}
* {{Patch 9.1.0|note=Added <code>tooltipLoc, modelSceneLayer, scriptedAnimationEffectID</code> fields.}}
* {{Patch 9.0.1|note=Added <code>textureKit, frameTextureKit, widgetScale, layoutDirection</code> fields.}}
* {{Patch 8.2.0|note=Added.}}
```