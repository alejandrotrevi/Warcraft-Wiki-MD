# API C Console.GetAllCommands

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Console|system=Console}}
Returns all console variables and commands.
 commands = C_Console.GetAllCommands()

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

==Details==
* Not all cvars are returned yet on initial login<ref>https://github.com/Stanzilla/AdvancedInterfaceOptions/issues/38</ref> until {{api|t=e|VARIABLES_LOADED}}, e.g. {{api|t=c|AutoPushSpellToActionBar}}

==Example==
Prints all cvars and commands.
<syntaxhighlight lang="lua">
/run for k, v in pairs(C_Console.GetAllCommands()) do print(k, v.command) end
</syntaxhighlight>

==Patch changes==
* {{Patch 9.1.0|note=Added <code>scriptParameters</code> and <code>Macro</code> fields.}}
* {{Patch 8.2.5|note=Removed "Category" prefix, e.g. <code>CategoryDebug</code> to <code>Debug</code>}}
* {{Patch 7.3.0|note=Added.}}

==References==
```