# API C UIWidgetManager.GetCaptureBarWidgetVisualizationInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetCaptureBarWidgetVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|CaptureBarWidgetVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| shownState || {{apitype|Enum.WidgetShownState}} || 
|-
| barValue || {{apitype|number}} || 
|-
| barMinValue || {{apitype|number}} || 
|-
| barMaxValue || {{apitype|number}} || 
|-
| neutralZoneSize || {{apitype|number}} || 
|-
| neutralZoneCenter || {{apitype|number}} || 
|-
| tooltip || {{apitype|string}} || 
|-
| glowAnimType || {{apitype|Enum.CaptureBarWidgetGlowAnimType}} || 
|-
| fillDirectionType || {{apitype|Enum.CaptureBarWidgetFillDirectionType}} || 
|-
| tooltipLoc || {{apitype|Enum.UIWidgetTooltipLocation}} || 
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

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.CaptureBarWidgetGlowAnimType
! Value !! Field !! Description
|-
| 0 || None || 
|-
| 1 || Pulse || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.CaptureBarWidgetFillDirectionType
! Value !! Field !! Description
|-
| 0 || RightToLeft || 
|-
| 1 || LeftToRight || 
|}

{{:Enum.UIWidgetTooltipLocation}}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}

==Patch changes==
* {{Patch 9.1.0|note=Added <code>tooltipLoc, modelSceneLayer, scriptedAnimationEffectID</code> fields.}}
* {{Patch 9.0.1|note=Added <code>textureKit, frameTextureKit, widgetScale, layoutDirection</code> fields.}}
* {{Patch 8.3.0|note=Added <code>fillDirectionType</code> field.}}
* {{Patch 8.2.0|note=Added <code>barValue, barMinValue, barMaxValue, neutralZoneSize, neutralZoneCenter, tooltip, glowAnimType, widgetSizeSetting, frameTextureKitID, inAnimType, outAnimType</code> fields.}}
* {{Patch 8.1.0|note=Added <code>hasTimer</code> field.}}
* {{Patch 8.0.1|note=Added.}}
```