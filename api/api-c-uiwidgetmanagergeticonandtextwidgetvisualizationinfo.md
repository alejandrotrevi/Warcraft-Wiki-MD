# API C UIWidgetManager.GetIconAndTextWidgetVisualizationInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetIconAndTextWidgetVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|IconAndTextWidgetVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| state || {{apitype|Enum.IconAndTextWidgetState}} || 
|-
| text || {{apitype|string}} || 
|-
| tooltip || {{apitype|string}} || 
|-
| dynamicTooltip || {{apitype|string}} || 
|-
| tooltipLoc || {{apitype|Enum.UIWidgetTooltipLocation}} || 
|-
| shiftTextType || {{apitype|Enum.IconAndTextShiftTextType}} || <font color="green">11.0.5</font>
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

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.IconAndTextWidgetState
! Value !! Field !! Description
|-
| 0 || Hidden || 
|-
| 1 || Shown || 
|-
| 2 || ShownWithDynamicIconFlashing || 
|-
| 3 || ShownWithDynamicIconNotFlashing || 
|}

{{:Enum.UIWidgetTooltipLocation}}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}

==Patch changes==
* {{Patch 9.1.0|note=Added <code>tooltipLoc, modelSceneLayer, scriptedAnimationEffectID</code> fields.}}
* {{Patch 9.0.1|note=Added <code>textureKit, frameTextureKit, widgetScale, layoutDirection</code> fields.}}
* {{Patch 8.2.0|note=Added <code>widgetSizeSetting, frameTextureKitID, inAnimType, outAnimType</code> fields.}}
* {{Patch 8.0.1|note=Added.}}
```