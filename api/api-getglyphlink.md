# API GetGlyphLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a link to a glyph specified by index and talent group.
 link = GetGlyphLink(index [, talentGroup])

==Arguments==
:;index:{{apitype|number}} - Ranging from <code>1</code> to <code>6</code>, the glyph's index. See Notes for more information.
:;talentGroup:{{apitype|number?}} - Optional, ranging from <code>1</code> (primary) to <code>2</code> (secondary) the talent group to query. Defaults to the currently active talent group.

==Returns==
:;link:{{apitype|string}} - The link to the glyph if it's populated, otherwise empty string.

==Details==
The indices are not in a logical order, see table and gallery picture below for reference.
{| class="sortable darktable zebra col1-center"
!Index!!Type!!Level
|-
|1||Major||15
|-
|2||Minor||15
|-
|3||Minor||50
|-
|4||Major||30
|-
|5||Minor||70
|-
|6||Major||80
|}

==Gallery==
<gallery>
File:Glyph ids.png|Indices for each glyph slot
</gallery>
```