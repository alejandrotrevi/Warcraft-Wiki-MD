# API C UIWidgetManager.GetHorizontalCurrenciesWidgetVisualizationInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetHorizontalCurrenciesWidgetVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|HorizontalCurrenciesWidgetVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|shownState}} || {{apitype|Enum.WidgetShownState}} || 
|-
| {{apiname|currencies}} || {{apitype|UIWidgetCurrencyInfo[]}} || 
|-
| {{apiname|tooltipLoc}} || {{apitype|Enum.UIWidgetTooltipLocation}} || <font color="green">9.1.0</font>
|-
| {{apiname|widgetSizeSetting}} || {{apitype|number}} || <font color="green">8.2.0</font>
|-
| {{apiname|textureKit}} || {{apitype|textureKit}} || <font color="green">9.0.1</font>
|-
| {{apiname|frameTextureKit}} || {{apitype|textureKit}} || <font color="green">9.0.1</font>
|-
| {{apiname|hasTimer}} || {{apitype|boolean}} || <font color="green">8.1.0</font>
|-
| {{apiname|orderIndex}} || {{apitype|number}} || 
|-
| {{apiname|widgetTag}} || {{apitype|string}} || 
|-
| {{apiname|inAnimType}} || {{apitype|Enum.WidgetAnimationType}} || <font color="green">8.2.0</font>
|-
| {{apiname|outAnimType}} || {{apitype|Enum.WidgetAnimationType}} || <font color="green">8.2.0</font>
|-
| {{apiname|widgetScale}} || {{apitype|Enum.UIWidgetScale}} || <font color="green">9.0.1</font>
|-
| {{apiname|layoutDirection}} || {{apitype|Enum.UIWidgetLayoutDirection}} || <font color="green">9.0.1</font>
|-
| {{apiname|modelSceneLayer}} || {{apitype|Enum.UIWidgetModelSceneLayer}} || <font color="green">9.1.0</font>
|-
| {{apiname|scriptedAnimationEffectID}} || {{apitype|number}} || <font color="green">9.1.0</font>
|}

{{:Enum.WidgetShownState}}

{{:Struct UIWidgetCurrencyInfo}}

{{:Enum.UIWidgetTooltipLocation}}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```