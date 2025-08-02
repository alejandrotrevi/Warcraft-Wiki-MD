# API GetFonts

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of available fonts.
 fonts = GetFonts()

==Returns==
:;fonts:{{apitype|string[]}} - a table containing font object names.

==Details==
* The names in the returned table may correspond to globally accessible font objects of the same name.
* The names in the returned table can be used in conjunction with {{api|GetFontInfo}} to query font attributes such as sizing or coloring information.

==See also==
* {{api|GetFontInfo}}
```