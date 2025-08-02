# API C LFGInfo.GetDungeonInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LFGInfo|system=LFGInfo}}
Needs summary.
 dungeonInfo = C_LFGInfo.GetDungeonInfo(lfgDungeonID)

==Arguments==
:;lfgDungeonID:{{apitype|number}}

==Returns==
:;dungeonInfo:{{apitype|LFGDungeonInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| iconID || {{apitype|number}} || 
|-
| link || {{apitype|string?}} || 
|}

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```