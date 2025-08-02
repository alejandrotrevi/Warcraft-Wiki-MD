# API C UIWidgetManager.GetUnitPowerBarWidgetVisualizationInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetUnitPowerBarWidgetVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|UnitPowerBarWidgetVisualizationInfo?}}
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
| tooltip || {{apitype|string}} || 
|-
| barValueTextType || {{apitype|Enum.StatusBarValueTextType}} || 
|-
| overrideBarText || {{apitype|string}} || 
|-
| overrideBarTextShownType || {{apitype|Enum.StatusBarOverrideBarTextShownType}} || 
|-
| tooltipLoc || {{apitype|Enum.UIWidgetTooltipLocation}} || 
|-
| fillMotionType || {{apitype|Enum.UIWidgetMotionType}} || 
|-
| flashBlendModeType || {{apitype|Enum.UIWidgetBlendModeType}} || 
|-
| sparkBlendModeType || {{apitype|Enum.UIWidgetBlendModeType}} || 
|-
| flashMomentType || {{apitype|Enum.WidgetUnitPowerBarFlashMomentType}} || 
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

{{:Enum.StatusBarValueTextType}}

{{:Enum.StatusBarOverrideBarTextShownType}}

{{:Enum.UIWidgetTooltipLocation}}

{{:Enum.UIWidgetMotionType}}

{{:Enum.UIWidgetBlendModeType}}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.WidgetUnitPowerBarFlashMomentType
! Value !! Field !! Description
|-
| 0 || FlashWhenMax || 
|-
| 1 || FlashWhenMin || 
|-
| 2 || NeverFlash || 
|}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}

==Patch changes==
* {{Patch 9.2.0|note=Added.}}
```