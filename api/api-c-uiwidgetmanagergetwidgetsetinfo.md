# API C UIWidgetManager.GetWidgetSetInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Needs summary.
 widgetSetInfo = C_UIWidgetManager.GetWidgetSetInfo(widgetSetID)

==Arguments==
:;widgetSetID:{{apitype|number}} : [[UiWidgetSetID]]
{{:UiWidgetSetID|nocaption=1}}

==Returns==
:;widgetSetInfo:{{apitype|UIWidgetSetInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|layoutDirection}} || {{apitype|Enum.UIWidgetSetLayoutDirection}} || 
|-
| {{apiname|verticalPadding}} || {{apitype|number}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.UIWidgetSetLayoutDirection
! Value !! Field !! Description
|-
| 0 || {{apiname|Vertical}} || 
|-
| 1 || {{apiname|Horizontal}} || 
|-
| 2 || {{apiname|Overlap}} || <font color="green">10.2.6</font>
|}

==Patch changes==
* {{Patch 9.0.2|note=Added.}}
```