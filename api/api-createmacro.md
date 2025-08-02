# API CreateMacro

**Contributor:** LudiusMaximus

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|nocombat|note=Restricted since patch 2.0.1}}
Creates a macro.
 macroId = CreateMacro(name, iconFileID [, body, perCharacter])

==Arguments==
:;name:{{apitype|string}} - The name of the macro to be displayed in the UI. The current UI imposes a 16-character limit.
:;iconFileID:{{apitype|number,string}} - A [[FileID]] or string identifying the icon texture to use. The available icons can be retrieved by calling {{api|GetMacroIcons}}() and {{api|GetMacroItemIcons}}(); other textures inside <code>Interface\ICONS</code> may also be used.
:;body:{{apitype|string?}} - The macro commands to be executed. If this string is longer than 255 characters, only the first 255 will be saved.
:;perCharacter:{{apitype|boolean?}} - true to create a per-character macro, nil to create a general macro available to all characters.

==Returns==
:;macroId:{{apitype|number}} - The 1-based index of the newly-created macro, as displayed in the "Create Macros" UI.

==Example==
Creates an empty macro with the respective FileID for <code>"trade_engineering"</code>
 /run CreateMacro("test", 136243)
Creates a character-specific macro. The question mark icon will dynamically display the Hearthstone icon.
 /run CreateMacro("to home", "INV_Misc_QuestionMark", "/cast Hearthstone", true)
Use a custom file from your Interface\Icons folder. (Using only the file path as second argument did not work when tested in 11.0.2.56647.)
 /run CreateMacro("MyMacro", GetFileIDFromPath("Interface\\Icons\\myIcon.blp"))

==Details==
* This function will generate an error if the maximum macros of the specified kind already exist (120 for per account and 18 for per character).
* It is possible to create macros with duplicate names. You should enumerate the current macros using [[API GetNumMacros|GetNumMacros()]] and [[API GetMacroInfo|GetMacroInfo(macroId)]] to ensure that your new macro name doesn't already exist. Macros with duplicate names can be used in most situations, but the behavior of macro functions that retrieve a macro by name is undefined when multiple macros of that name exist.

==Patch changes==
* {{Patch 3.0.2|note=Macros are now saved on the server by default. The positions of <code>perCharacter</code> and <code>localStore</code> arguments were switched.}}
* {{Patch 2.0.1|note=Now protected while in combat.}}

==See also==
* {{api|EditMacro}}
```