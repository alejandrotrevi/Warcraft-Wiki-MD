# API CreateFont

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Creates a {{api|t=o|Font}} object.
 fontObject = CreateFont(name)

==Arguments==
:;name:{{apitype|string}} - Globally-accessible name to be assigned for use as <code>[[API getglobal|_G]]["name"]</code>

==Returns==
:;fontObject:{{apitype|Font}} - Reference to the new font object.

==Details==
* Font objects, similar to XML {{api|t=x|Font}} elements, may be used to create a common font pattern assigned to several widgets via {{api|t=w|FontInstance:SetFontObject(fontObject)}}.
** Subsequently changing the font object will affect the text displayed on every widget it was assigned to.
* Since the new font object is created without any properties, it should be initialized via {{api|t=w|FontInstance:SetFont(path, height [, flags])}} or {{api|t=w|Font:CopyFontObject(otherFont)}}.
```