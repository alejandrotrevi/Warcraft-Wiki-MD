# API C UIWidgetManager.GetTextWithSubtextWidgetVisualizationInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetTextWithSubtextWidgetVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|TextWithSubtextWidgetVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| shownState || {{apitype|Enum.WidgetShownState}} || 
|-
| enabledState || {{apitype|Enum.WidgetEnabledState}} || 
|-
| text || {{apitype|string}} || 
|-
| widgetWidth || {{apitype|number}} || 
|-
| tooltip || {{apitype|string}} || 
|-
| textSizeType || {{apitype|Enum.UIWidgetTextSizeType}} || 
|-
| fontType || {{apitype|Enum.UIWidgetFontType}} || 
|-
| tooltipLoc || {{apitype|Enum.UIWidgetTooltipLocation}} || 
|-
| hAlign || {{apitype|Enum.WidgetTextHorizontalAlignmentType}} || 
|-
| subText || {{apitype|string}} || 
|-
| subTextSizeType || {{apitype|Enum.UIWidgetTextSizeType}} || 
|-
| subTextFontType || {{apitype|Enum.UIWidgetFontType}} || 
|-
| subTextHAlign || {{apitype|Enum.WidgetTextHorizontalAlignmentType}} || 
|-
| subTextEnabledState || {{apitype|Enum.WidgetEnabledState}} || 
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
|-
| spacing || {{apitype|number}} || 
|}

{{:Enum.WidgetShownState}}

{{:Enum.WidgetEnabledState}}

{{:Enum.UIWidgetTextSizeType}}

{{:Enum.UIWidgetFontType}}

{{:Enum.UIWidgetTooltipLocation}}

{{:Enum.WidgetTextHorizontalAlignmentType}}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}
```