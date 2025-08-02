# API C UIWidgetManager.GetTextWithStateWidgetVisualizationInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetTextWithStateWidgetVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|TextWithStateWidgetVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| shownState || {{apitype|Enum.WidgetShownState}} || 
|-
| enabledState || {{apitype|Enum.WidgetEnabledState}} || 
|-
| text || {{apitype|string}} || 
|-
| tooltip || {{apitype|string}} || 
|-
| textSizeType || {{apitype|Enum.UIWidgetTextSizeType}} || 
|-
| fontType || {{apitype|Enum.UIWidgetFontType}} || 
|-
| bottomPadding || {{apitype|number}} || 
|-
| tooltipLoc || {{apitype|Enum.UIWidgetTooltipLocation}} || 
|-
| hAlign || {{apitype|Enum.WidgetTextHorizontalAlignmentType}} || 
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

{{:Enum.WidgetEnabledState}}

{{:Enum.UIWidgetTextSizeType}}

{{:Enum.UIWidgetFontType}}

{{:Enum.UIWidgetTooltipLocation}}

{{:Enum.WidgetTextHorizontalAlignmentType}}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}

==Patch changes==
* {{Patch 9.1.0|note=Added <code>tooltipLoc, hAlign, modelSceneLayer, scriptedAnimationEffectID</code> fields.}}
* {{Patch 9.0.1|note=Added <code>fontType, bottomPadding, textureKit, frameTextureKit, widgetScale, layoutDirection</code> fields.}}
* {{Patch 8.2.5|note=Added <code>textSizeType</code> field.}}
* {{Patch 8.2.0|note=Added <code>tooltip, widgetSizeSetting, textureKitID, frameTextureKitID, inAnimType, outAnimType</code> fields.}}
* {{Patch 8.1.0|note=Added <code>hasTimer</code> field.}}
* {{Patch 8.0.1|note=Added.}}
```