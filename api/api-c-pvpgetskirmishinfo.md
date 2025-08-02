# API C PvP.GetSkirmishInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PvP|system=PvpInfo}}
Needs summary.
 battlemasterListInfo = C_PvP.GetSkirmishInfo(pvpBracket)

==Arguments==
:;pvpBracket:{{apitype|number}}

==Returns==
:;battlemasterListInfo:{{apitype|BattlemasterListInfo}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|name}} || {{apitype|string}} || 
|-
| {{apiname|matchmakingType}} || {{apitype|Enum.PvPMatchmakingType}} || 
|-
| {{apiname|minPlayers}} || {{apitype|number}} || 
|-
| {{apiname|maxPlayers}} || {{apitype|number}} || 
|-
| {{apiname|icon}} || {{apitype|fileID}} || 
|-
| {{apiname|longDescription}} || {{apitype|string}} || 
|-
| {{apiname|shortDescription}} || {{apitype|string}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.PvPMatchmakingType
! Value !! Field !! Description
|-
| 0 || {{apiname|Battleground}} || 
|-
| 1 || {{apiname|Arena}} || 
|}

==Patch changes==
* {{Patch 11.1.7|note=Changed <code>instanceType</code> (number) field to <code>matchmakingType</code> (enum).}}
* {{Patch 7.2.0|note=Added.}}
```