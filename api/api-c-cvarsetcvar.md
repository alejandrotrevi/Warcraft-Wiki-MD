# API C CVar.SetCVar

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets a console variable.
 success = C_CVar.SetCVar(name [, value])
         = {{tlygo|SetCVar}}

==Arguments==
:;name:{{apitype|string}} : [[Console_variables#Console_Variables|CVar]] - Name of the CVar.
:;value:{{apitype|string,number?|default="0"}} - The new value of the CVar.

==Returns==
:;success:{{apitype|boolean}} - Whether the CVar was successfully set. Returns <code>nil</code> if attempting to set a secure cvar in combat.

==Details==
* Some settings require a reload/relog before they take effect.
* CVars are not saved to Config.wtf until properly logging out or reloading the game.
* [[API GetCVarInfo|Secure CVars]] cannot be set in combat and only with <code>SetCVar</code> instead of <code>/console</code>.
* Character and Account specific variables are stored server-side depending on CVar {{api|t=c|synchronizeConfig}}.

==See Also==
* {{api|C_CVar.GetCVar}}

==Patch changes==
* {{Patch 10.0.0|note=Removed <code>scriptCVar</code> argument.}}
* {{Patch 8.1.5|note=Namespaced to <code>C_CVar.SetCVar</code>.}}
* {{Patch 1.0.0|note=Added.}}
```