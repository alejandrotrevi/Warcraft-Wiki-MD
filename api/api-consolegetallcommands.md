# API ConsoleGetAllCommands

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Console}}
Needs summary.
 commands = ConsoleGetAllCommands()

==Returns==
:;commands:{{apitype|ConsoleCommandInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| command || {{apitype|string}} || 
|-
| help || {{apitype|string}} || 
|-
| category || {{apitype|Enum.ConsoleCategory}} || 
|-
| commandType || {{apitype|Enum.ConsoleCommandType}} || 
|-
| scriptContents || {{apitype|string}} || 
|-
| scriptParameters || {{apitype|string}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.ConsoleCategory
! Value !! Field !! Description
|-
| 0 || Debug || 
|-
| 1 || Graphics || 
|-
| 2 || Console || 
|-
| 3 || Combat || 
|-
| 4 || Game || 
|-
| 5 || Default || 
|-
| 6 || Net || 
|-
| 7 || Sound || 
|-
| 8 || Gm || 
|-
| 9 || Reveal || 
|-
| 10 || None || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.ConsoleCommandType
! Value !! Field !! Description
|-
| 0 || Cvar || 
|-
| 1 || Command || 
|-
| 2 || Macro || 
|-
| 3 || Script || 
|}
```