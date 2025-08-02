# API C Console.GetColorFromType

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Console|system=Console}}
Returns color info for a color type.
 color = C_Console.GetColorFromType(colorType)

==Arguments==
:;colorType:{{apitype|Enum.ConsoleColorType}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || DefaultColor || 
|-
| 1 || InputColor || 
|-
| 2 || EchoColor || 
|-
| 3 || ErrorColor || 
|-
| 4 || WarningColor || 
|-
| 5 || GlobalColor || 
|-
| 6 || AdminColor || 
|-
| 7 || HighlightColor || 
|-
| 8 || BackgroundColor || 
|-
| 9 || ClickbufferColor || 
|-
| 10 || PrivateColor || 
|-
| 11 || DefaultGreen || 
|}

==Returns==
:;color:{{apitype|ColorMixin}}

==Patch changes==
* {{Patch 8.0.1|note=Added <code>DefaultGreen</code> field.}}
* {{Patch 7.3.0|note=Added.}}
```