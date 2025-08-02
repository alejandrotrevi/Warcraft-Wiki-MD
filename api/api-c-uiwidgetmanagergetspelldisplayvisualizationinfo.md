# API C UIWidgetManager.GetSpellDisplayVisualizationInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetInfo = C_UIWidgetManager.GetSpellDisplayVisualizationInfo(widgetID)

==Arguments==
:;widgetID:{{apitype|number}} - Returned from {{api|t=e|UPDATE_UI_WIDGET}} and {{api|C_UIWidgetManager.GetAllWidgetsBySetID}}()

==Returns==
:;widgetInfo:{{apitype|SpellDisplayVisualizationInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| spellInfo || {{apitype|UIWidgetSpellInfo}} || 
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

{| class="vertical-align-row"
|
{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ UIWidgetSpellInfo
! Field !! Type !! Description
|-
| spellID || {{apitype|number}} || 
|-
| tooltip || {{apitype|string}} || 
|-
| text || {{apitype|string}} || 
|-
| stackDisplay || {{apitype|number}} || 
|-
| iconSizeType || {{apitype|Enum.WidgetIconSizeType}} || 
|-
| iconDisplayType || {{apitype|Enum.SpellDisplayIconDisplayType}} || 
|-
| textShownState || {{apitype|Enum.SpellDisplayTextShownStateType}} || <font color="green">9.0.1</font>
|-
| borderColor || {{apitype|Enum.SpellDisplayBorderColor}} || <font color="green">10.0.0</font>
|-
| textFontType || {{apitype|Enum.UIWidgetFontType}} || <font color="green">9.2.5</font>
|-
| textSizeType || {{apitype|Enum.UIWidgetTextSizeType}} || <font color="green">9.2.5</font>
|-
| hAlignType || {{apitype|Enum.WidgetTextHorizontalAlignmentType}} || <font color="green">9.2.5</font>
|-
| isLootObject || {{apitype|boolean}} || <font color="green">10.0.0</font>
|}
|
{{:Enum.WidgetIconSizeType}}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.SpellDisplayIconSizeType
! Value !! Field !! Description
|-
| 0 || Small || 
|-
| 1 || Medium || 
|-
| 2 || Large || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.SpellDisplayIconDisplayType
! Value !! Field !! Description
|-
| 0 || Buff || 
|-
| 1 || Debuff || 
|-
| 2 || Circular || <font color="green">9.0.1</font>
|-
| 3 || NoBorder || <font color="green">9.2.0</font>
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.SpellDisplayTextShownStateType
! Value !! Field !! Description
|-
| 0 || Shown || 
|-
| 1 || Hidden || 
|}
|}

{{:Enum.UIWidgetFontType}}

{{:Enum.UIWidgetTextSizeType}}

{{:Enum.WidgetTextHorizontalAlignmentType}}

{{:Enum.UIWidgetTooltipLocation}}

{{:Enum.WidgetAnimationType}}

{{:Enum.UIWidgetScale}}

{{:Enum.UIWidgetLayoutDirection}}

{{:Enum.UIWidgetModelSceneLayer}}

==Patch changes==
* {{Patch 11.0.2|note=Removed <code>shownState, enabledState</code> fields.}}
* {{Patch 9.1.0|note=Added <code>tooltipLoc, modelSceneLayer, scriptedAnimationEffectID</code> fields.}}
* {{Patch 9.0.1|note=Added <code>textureKit, frameTextureKit, widgetScale, layoutDirection</code>.}}
* {{Patch 8.2.0|note=Added <code>widgetSizeSetting, textureKitID, frameTextureKitID, inAnimType, outAnimType</code> fields.}}
* {{Patch 8.1.0|note=Added.}}
```