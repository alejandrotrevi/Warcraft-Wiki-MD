# API C UIWidgetManager.GetItemDisplayVisualizationInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetItemDisplayVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|ItemDisplayVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| shownState || {{apitype|Enum.WidgetShownState}} || 
|-
| tooltipLoc || {{apitype|Enum.UIWidgetTooltipLocation}} || 
|-
| itemInfo || {{apitype|UIWidgetItemInfo}} || 
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

{{:Enum.UIWidgetTooltipLocation}}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ UIWidgetItemInfo
! Field !! Type !! Description
|-
| {{apiname|itemID}} || {{apitype|number}} || 
|-
| {{apiname|stackCount}} || {{apitype|number?}} || 
|-
| {{apiname|overrideItemName}} || {{apitype|string?}} || 
|-
| {{apiname|infoText}} || {{apitype|string?}} || 
|-
| {{apiname|overrideTooltip}} || {{apitype|string?}} || 
|-
| {{apiname|textDisplayStyle}} || {{apitype|Enum.ItemDisplayTextDisplayStyle}} || 
|-
| {{apiname|tooltipEnabled}} || {{apitype|boolean}} || 
|-
| {{apiname|iconSizeType}} || {{apitype|Enum.WidgetIconSizeType}} || 
|-
| {{apiname|infoTextEnabledState}} || {{apitype|Enum.WidgetEnabledState}} || 
|-
| {{apiname|showAsEarned}} || {{apitype|boolean}} || <font color="green">10.2.0</font>
|-
| {{apiname|itemNameTextFontType}} || {{apitype|Enum.UIWidgetFontType}} || <font color="green">10.2.5</font>
|-
| {{apiname|itemNameTextSizeType}} || {{apitype|Enum.UIWidgetTextSizeType}} || <font color="green">10.2.5</font>
|-
| {{apiname|infoTextFontType}} || {{apitype|Enum.UIWidgetFontType}} || <font color="green">10.2.5</font>
|-
| {{apiname|infoTextSizeType}} || {{apitype|Enum.UIWidgetTextSizeType}} || <font color="green">10.2.5</font>
|-
| {{apiname|itemNameCustomColor}} || {{apitype|Enum.WidgetEnabledState}} || <font color="green">11.0.2</font>
|-
| {{apiname|itemNameCustomColorOverrideState}} || {{apitype|Enum.UIWidgetOverrideState}} || <font color="green">11.0.2</font>
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.ItemDisplayTextDisplayStyle
! Value !! Field !! Description
|-
| 0 || WorldQuestReward || 
|-
| 1 || ItemNameAndInfoText || 
|-
| 2 || ItemNameOnlyCentered || 
|}

{{:Enum.WidgetIconSizeType}}

{{:Enum.WidgetEnabledState}}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}
```