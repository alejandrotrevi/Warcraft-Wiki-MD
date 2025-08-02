# API C UIWidgetManager.GetTugOfWarWidgetVisualizationInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetTugOfWarWidgetVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|TugOfWarWidgetVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| shownState || {{apitype|Enum.WidgetShownState}} || 
|-
| minValue || {{apitype|number}} || 
|-
| maxValue || {{apitype|number}} || 
|-
| currentValue || {{apitype|number}} || 
|-
| neutralZoneCenter || {{apitype|number}} || 
|-
| neutralZoneSize || {{apitype|number}} || 
|-
| leftIconInfo || {{apitype|UIWidgetIconInfo}} || 
|-
| rightIconInfo || {{apitype|UIWidgetIconInfo}} || 
|-
| glowAnimType || {{apitype|Enum.WidgetGlowAnimType}} || 
|-
| tooltip || {{apitype|string}} || 
|-
| tooltipLoc || {{apitype|Enum.UIWidgetTooltipLocation}} || 
|-
| neutralFillStyle || {{apitype|Enum.TugOfWarStyleValue}} || <font color="green">10.2.5</font>
|-
| markerArrowShownState || {{apitype|Enum.TugOfWarMarkerArrowShownState}} || <font color="green">10.2.5</font>
|-
| widgetSizeSetting || {{apitype|number}} || 
|-
| textureKit || {{apitype|textureKit}} || 
|-
| frameTextureKit || {{apitype|textureKit}} || 
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

{{:Struct UIWidgetIconInfo}}

{{:Enum.WidgetGlowAnimType}}

{{:Enum.UIWidgetTooltipLocation}}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.TugOfWarStyleValue
! Value !! Field !! Description
|-
| 0 || DefaultYellow || 
|-
| 1 || ArchaeologyBrown || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.TugOfWarMarkerArrowShownState
! Value !! Field !! Description
|-
| 0 || Never || 
|-
| 1 || Always || 
|-
| 2 || FlashOnMove || 
|}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}
```