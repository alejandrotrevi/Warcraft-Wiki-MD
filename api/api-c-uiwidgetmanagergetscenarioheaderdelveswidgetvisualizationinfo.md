# API C UIWidgetManager.GetScenarioHeaderDelvesWidgetVisualizationInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetScenarioHeaderDelvesWidgetVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|ScenarioHeaderDelvesWidgetVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|shownState}} || {{apitype|Enum.WidgetShownState}} || 
|-
| {{apiname|headerText}} || {{apitype|string}} || 
|-
| {{apiname|tooltip}} || {{apitype|string}} || 
|-
| {{apiname|tooltipLoc}} || {{apitype|Enum.UIWidgetTooltipLocation}} || 
|-
| {{apiname|tierText}} || {{apitype|string}} || 
|-
| {{apiname|tierTooltipSpellID}} || {{apitype|number?}} || 
|-
| {{apiname|currencies}} || {{apitype|UIWidgetCurrencyInfo[]}} || 
|-
| {{apiname|spells}} || {{apitype|UIWidgetSpellInfo[]}} || 
|-
| {{apiname|rewardInfo}} || {{apitype|UIWidgetRewardInfo}} || 
|-
| {{apiname|widgetSizeSetting}} || {{apitype|number}} || 
|-
| {{apiname|textureKit}} || {{apitype|textureKit}} || 
|-
| {{apiname|frameTextureKit}} || {{apitype|textureKit}} || 
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
| {{apiname|widgetScale}} || {{apitype|Enum.UIWidgetScale}} || 
|-
| {{apiname|layoutDirection}} || {{apitype|Enum.UIWidgetLayoutDirection}} || 
|-
| {{apiname|modelSceneLayer}} || {{apitype|Enum.UIWidgetModelSceneLayer}} || 
|-
| {{apiname|scriptedAnimationEffectID}} || {{apitype|number}} || 
|}

{{:Enum.UIWidgetTooltipLocation}}

{{:Struct UIWidgetCurrencyInfo}}

{{:Struct UIWidgetSpellInfo}}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ UIWidgetRewardInfo
! Field !! Type !! Description
|-
| {{apiname|shownState}} || {{apitype|Enum.UIWidgetRewardShownState}} || 
|-
| {{apiname|earnedTooltip}} || {{apitype|string}} || 
|-
| {{apiname|unearnedTooltip}} || {{apitype|string}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.UIWidgetRewardShownState
! Value !! Field !! Description
|-
| 0 || {{apiname|Hidden}} || 
|-
| 1 || {{apiname|ShownEarned}} || 
|-
| 2 || {{apiname|ShownUnearned}} || 
|}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}
```