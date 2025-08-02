# API C UIColor.GetColors

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of UI colors to be imported into the global environment on login.
 colors = C_UIColor.GetColors()

==Returns==
:;colors:{{apitype|DBColorExport[]}} - A list of UI color structures.
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| baseTag || {{apitype|string}} || The global name to associate with this color.
|-
| color || {{apitype|ColorMixin}} || 
|}

==Details==
* UI colors are stored within the {{dbc|globalcolor|globalcolor}} client database.

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```