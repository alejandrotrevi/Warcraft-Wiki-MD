# API SetUnitCursorTexture

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Needs summary.
 hasCursor = SetUnitCursorTexture(textureObject, unit [, style, includeLowPriority])

==Arguments==
:;textureObject:{{apitype|Unknown}}
:;unit:{{apitype|string}}
:;style:{{apitype|Enum.CursorStyle?}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || Mouse || 
|-
| 1 || Crosshair || 
|}
:;includeLowPriority:{{apitype|boolean?}}

==Returns==
:;hasCursor:{{apitype|boolean}}
```