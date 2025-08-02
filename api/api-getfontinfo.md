# API GetFontInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a structured table of information about the given font object.
 fontInfo = GetFontInfo(font)

==Arguments==
:;font:{{apitype|Font,string}} - Either a font object or the name of a global font object.

==Returns==
:;fontInfo:{{apitype|FontScriptInfo}}
{{:Struct_FontScriptInfo|nocaption=1}}

==Details==
* If a font has no outline or monochrome flags applied, the <code>outline</code> field in the returned table will always be an empty string.

==See also==
* {{api|GetFonts}}
```