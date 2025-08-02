# API C UIWidgetManager.GetIconTextAndBackgroundWidgetVisualizationInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetIconTextAndBackgroundWidgetVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|IconTextAndBackgroundWidgetVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| shownState || {{apitype|Enum.WidgetShownState}} || 
|-
| text || {{apitype|string}} || 
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

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}

==Patch changes==
* {{Patch 9.1.0|note=Added <code>modelSceneLayer, scriptedAnimationEffectID</code> fields.}}
* {{Patch 9.0.1|note=Added <code>textureKit, frameTextureKit, widgetScale, layoutDirection</code> fields.}}
* {{Patch 8.2.0|note=Added <code>widgetSizeSetting, frameTextureKitID, inAnimType, outAnimType</code> fields.}}
* {{Patch 8.1.0|note=Added <code>text, hasTimer</code> fields.}}
* {{Patch 8.0.1|note=Added.}}
```