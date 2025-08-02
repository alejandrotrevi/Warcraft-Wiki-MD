# API GetMacroInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a macro.
 name, icon, body = GetMacroInfo(macro)

==Arguments==
:;macro:{{apitype|number,string}} - Macro slot index or the name of the macro. Slots 1 through 120 are general macros; 121 through 150 are per-character macros.

==Returns==
:;name:{{apitype|string}} - The name of the macro.
:;icon:{{apitype|fileID}} - Macro icon texture.
:;body:{{apitype|string}} - Macro contents.

==Patch changes==
* {{Patch 3.0.2|note=Removed <code>isLocal</code> return.}}
```