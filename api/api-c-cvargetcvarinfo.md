# API C CVar.GetCVarInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information on a console variable.
 value, defaultValue, isStoredServerAccount, isStoredServerCharacter, isLockedFromUser, isSecure, isReadOnly = C_CVar.GetCVarInfo(name)

==Arguments==
:;name:{{apitype|string}} - Name of the [[Console_variables#List_of_Console_Variables|CVar]] to query the value of. Only accepts console variables (i.e. not console commands).

==Returns==
:;value:{{apitype|string}} - Current value of the CVar.
:;defaultValue:{{apitype|string}} - Default value of the CVar.
:;isStoredServerAccount:{{apitype|boolean}} - If the CVar scope is set WoW account-wide. Stored on the server per CVar {{api|t=c|synchronizeConfig}}
:;isStoredServerCharacter:{{apitype|boolean}} - If the CVar scope is character-specific. Stored on the server per CVar {{api|t=c|synchronizeConfig}}
:;isLockedFromUser:{{apitype|boolean}}
:;isSecure:{{apitype|boolean}} - If the CVar cannot be set with {{api|SetCVar}} while in combat, which would fire {{api|t=e|ADDON_ACTION_BLOCKED}}. It's also not possible to set these via <code>/console</code>. Most nameplate cvars are secure.
:;isReadOnly:{{apitype|boolean}} - Returns true for {{api|t=c|portal}}, {{api|t=c|serverAlert}}, {{api|t=c|timingTestError}}. These CVars cannot be changed.

==Patch changes==
* {{Patch 10.2.0|note=Moved to the C_CVar namespace. An alias from the old function name still exists but will be removed in a future patch.}}
* {{Patch 3.0.2|note=Added.}}
```