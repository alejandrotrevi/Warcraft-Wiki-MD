# API C UIWidgetManager.GetTextureAndTextVisualizationInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetTextureAndTextVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|TextureAndTextVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|shownState}} || {{apitype|Enum.WidgetShownState}} || 
|-
| {{apiname|text}} || {{apitype|string}} || 
|-
| {{apiname|tooltip}} || {{apitype|string}} || 
|-
| {{apiname|tooltipLoc}} || {{apitype|Enum.UIWidgetTooltipLocation}} || <font color="green">9.1.0</font>
|-
| {{apiname|textSizeType}} || {{apitype|Enum.UIWidgetTextureAndTextSizeType}} || <font color="green">10.2.6</font>
|-
| {{apiname|textFormatType}} || {{apitype|Enum.UIWidgetTextFormatType}} || <font color="green">11.1.5</font>
|-
| {{apiname|updateAnimType}} || {{apitype|Enum.UIWidgetUpdateAnimType}} || <font color="green">11.1.5</font>
|-
| {{apiname|widgetSizeSetting}} || {{apitype|number}} || 
|-
| {{apiname|textureKit}} || {{apitype|textureKit}} || <font color="green">9.0.1</font>
|-
| {{apiname|frameTextureKit}} || {{apitype|textureKit}} || <font color="green">9.0.1</font>
|-
| {{apiname|hasTimer}} || {{apitype|boolean}} || 
|-
| {{apiname|orderIndex}} || {{apitype|number}} || 
|-
| {{apiname|widgetTag}} || {{apitype|string}} || 
|-
| {{apiname|inAnimType}} || {{apitype|Enum.WidgetAnimationType}} || 
|-
| {{apiname|outAnimType}} || {{apitype|Enum.WidgetAnimationType}} || 
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

{{:Enum.UIWidgetTooltipLocation}}

{{:Enum.UIWidgetTextureAndTextSizeType}}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.UIWidgetTextFormatType
! Value !! Field !! Description
|-
| 0 || {{apiname|None}} || 
|-
| 1 || {{apiname|TimeOneLevel}} || 
|-
| 2 || {{apiname|TimeTwoLevel}} || 
|-
| 3 || {{apiname|LeadingZeroesWithSixDigits}} || 
|}

{{:Enum.UIWidgetUpdateAnimType}}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}

==Patch changes==
* {{Patch 8.2.0|note=Added.}}
```