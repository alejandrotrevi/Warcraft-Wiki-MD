# API C UIWidgetManager.GetTextColumnRowVisualizationInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetTextColumnRowVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|TextColumnRowVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| shownState || {{apitype|Enum.WidgetShownState}} || 
|-
| entries || {{apitype|TextColumnRowEntryInfo[]}} || 
|-
| textSizeType || {{apitype|Enum.UIWidgetTextSizeType}} || 
|-
| fontType || {{apitype|Enum.UIWidgetFontType}} || 
|-
| tooltip || {{apitype|string}} || 
|-
| tooltipLoc || {{apitype|Enum.UIWidgetTooltipLocation}} || 
|-
| bottomPadding || {{apitype|number}} || 
|-
| widgetSizeSetting || {{apitype|number}} || 
|-
| textureKit || {{apitype|string}} || 
|-
| frameTextureKit || {{apitype|string}} || 
|-
| hasTimer || {{apitype|boolean}} || 
|-
| orderIndex || {{apitype|number}} || 
|-
| widgetTag || {{apitype|string}} || 
|-
| inAnimType || {{apitype|Enum.WidgetAnimationType}} || 
|-
| outAnimType || {{apitype|Enum.WidgetAnimationType}} || 
|-
| widgetScale || {{apitype|Enum.UIWidgetScale}} || 
|-
| layoutDirection || {{apitype|Enum.UIWidgetLayoutDirection}} || 
|-
| modelSceneLayer || {{apitype|Enum.UIWidgetModelSceneLayer}} || 
|-
| scriptedAnimationEffectID || {{apitype|number}} || 
|}

{{:Enum.WidgetShownState}}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ TextColumnRowEntryInfo
! Field !! Type !! Description
|-
| text || {{apitype|string}} || 
|-
| enabledState || {{apitype|Enum.WidgetEnabledState}} || 
|-
| hAlign || {{apitype|Enum.WidgetTextHorizontalAlignmentType}} || 
|-
| columnWidth || {{apitype|number}} || 
|}

{{:Enum.WidgetEnabledState}}

{{:Enum.WidgetTextHorizontalAlignmentType}}

{{:Enum.UIWidgetTextSizeType}}

{{:Enum.UIWidgetFontType}}

{{:Enum.UIWidgetTooltipLocation}}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```