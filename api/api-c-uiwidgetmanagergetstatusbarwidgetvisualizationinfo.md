# API C UIWidgetManager.GetStatusBarWidgetVisualizationInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetStatusBarWidgetVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|StatusBarWidgetVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| shownState || {{apitype|Enum.WidgetShownState}} || 
|-
| barMin || {{apitype|number}} || 
|-
| barMax || {{apitype|number}} || 
|-
| barValue || {{apitype|number}} || 
|-
| text || {{apitype|string}} || 
|-
| tooltip || {{apitype|string}} || 
|-
| barValueTextType || {{apitype|Enum.StatusBarValueTextType}} || 
|-
| overrideBarText || {{apitype|string}} || 
|-
| overrideBarTextShownType || {{apitype|Enum.StatusBarOverrideBarTextShownType}} || 
|-
| colorTint || {{apitype|Enum.StatusBarColorTintValue}} || 
|-
| partitionValues || {{apitype|number[]}} || 
|-
| tooltipLoc || {{apitype|Enum.UIWidgetTooltipLocation}} || 
|-
| fillMotionType || {{apitype|Enum.UIWidgetMotionType}} || 
|-
| barTextEnabledState || {{apitype|Enum.WidgetEnabledState}} || 
|-
| barTextFontType || {{apitype|Enum.UIWidgetFontType}} || 
|-
| barTextSizeType || {{apitype|Enum.UIWidgetTextSizeType}} || 
|-
| textEnabledState || {{apitype|Enum.WidgetEnabledState}} || 
|-
| textFontType || {{apitype|Enum.UIWidgetFontType}} || 
|-
| textSizeType || {{apitype|Enum.UIWidgetTextSizeType}} || 
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

{{:Enum.StatusBarValueTextType}}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.StatusBarOverrideBarTextShownType
! Value !! Field !! Description
|-
| 0 || Never || 
|-
| 1 || Always || 
|-
| 2 || OnlyOnMouseover || 
|-
| 3 || OnlyNotOnMouseover || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.StatusBarColorTintValue
! Value !! Field !! Description
|-
| 0 || None || 
|-
| 1 || Black || 
|-
| 2 || White || 
|-
| 3 || Red || 
|-
| 4 || Yellow || 
|-
| 5 || Orange || 
|-
| 6 || Purple || 
|-
| 7 || Green || 
|-
| 8 || Blue || 
|}

{{:Enum.UIWidgetTooltipLocation}}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}

==Patch changes==
* {{Patch 10.1.0|note=Added <code>textEnabledState, textFontType, textSizeType </code> fields.}}
* {{Patch 9.2.0|note=Added <code>fillMotionType, barTextEnabledState, barTextFontType, barTextSizeType </code> fields.}}
* {{Patch 9.1.0|note=Added <code>modelSceneLayer, scriptedAnimationEffectID, tooltipLoc</code> fields.}}
* {{Patch 9.0.1|note=Added <code>colorTint, frameTextureKit, layoutDirection, partitionValues, textureKit, widgetScale</code> fields.}}
* {{Patch 8.2.0|note=Added <code>inAnimType, outAnimType, overrideBarText, overrideBarTextShownType, textureKitID, widgetSizeSetting</code> fields.}}
* {{Patch 8.1.0|note=Added <code>barValueTextType, hasTimer, tooltip</code> fields.}}
* {{Patch 8.0.1|note=Added.}}
```