# API C UIWidgetManager.GetAllWidgetsBySetID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UIWidgetManager|system=UIWidgetManager}}
Returns all widgets for a widget set ID.
 widgets = C_UIWidgetManager.GetAllWidgetsBySetID(setID)

==Arguments==
:;setID:{{apitype|number}} : [[UiWidgetSetID]]
{{:UiWidgetSetID|nocaption=1}}

==Returns==
:;widgets:{{apitype|UIWidgetInfo[]}}
{{:Struct UIWidgetManager.UIWidgetInfo|nocaption=1}}

==Example==
<onlyinclude>Prints all UI widget IDs for the top center part of the screen, e.g. on Warsong Gulch:
<syntaxhighlight lang="lua">
local topCenter = C_UIWidgetManager.GetTopCenterWidgetSetID()
local widgets = C_UIWidgetManager.GetAllWidgetsBySetID(topCenter)
for _, w in pairs(widgets) do
	print(w.widgetType, w.widgetID)
end
</syntaxhighlight>
 > 0, 6     -- IconAndText,        VisID    3: Icon And Text: No Texture Kit
 > 3, 2     -- DoubleStatusBar,    VisID 1197: PvP - CTF - Double Status Bar
 > 14, 1640 -- DoubleStateIconRow, VisID 1201: PvP - CTF - Flag Status
[[File:API_C_UIWidgetManager_02.png]]</onlyinclude>

==Patch changes==
* {{Patch 8.0.1|note=Added.}}

==See also==
* {{api|t=e|UPDATE_UI_WIDGET}}
```