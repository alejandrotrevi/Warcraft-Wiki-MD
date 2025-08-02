# API C CVar.GetCVar

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current value of a console variable.
 value = C_CVar.GetCVar(name)
       = {{tlygo|GetCVar}}

==Arguments==
:;name:{{apitype|string}} : [[Console_variables#Console_Variables|CVar]] - name of the CVar to query the value of.

==Returns==
:;value:{{apitype|string?}} - current value of the CVar.

==Details==
* Calling this function with an invalid variable name, or a variable that cannot be queried by AddOns (like "accountName"), will return nil.

==See Also==
* {{api|C_CVar.SetCVar}}

==Patch changes==
* {{Patch 8.1.5|note=Namespaced to <code>C_CVar.GetCVar()</code>.}}
* {{Patch 1.0.0|note=Added.}}
```