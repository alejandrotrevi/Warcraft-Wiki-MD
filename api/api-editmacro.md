# API EditMacro

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat}}
Modifies an existing macro.
 macroID = EditMacro(macroInfo [, name , icon, body])

==Arguments==
:;macroInfo:{{apitype|number,string}} - The index or name of the macro to be edited. Index ranges from 1 to 120 for account-wide macros and 121 to 138 for character-specific.
:;name:{{apitype|string?}} - The name to assign to the macro. The current UI imposes a 16-character limit. The existing name remains unchanged if this argument is nil.
:;icon:{{apitype|number,string?}} : [[FileID]] - The path to the icon texture to assign to the macro. The existing icon remains unchanged if this argument is nil.
:;body:{{apitype|string?}} - The macro commands to be executed. If this string is longer than 255 characters, only the first 255 will be saved.

==Returns==
:;macroID:{{apitype|number}} - The new index of the macro, as displayed in the "Create Macros" UI. Same as argument "index" unless the macro name is changed, as they are sorted alphabetically.

==Details==
* If this function is called from within the macro that is edited, the rest of the macro (from the final character's position of the /run command onward) will run the new version.

==Example==
<syntaxhighlight lang="lua">
local macroID = EditMacro(1, "GoHome", 134414, "/use Hearthstone")
</syntaxhighlight>
```