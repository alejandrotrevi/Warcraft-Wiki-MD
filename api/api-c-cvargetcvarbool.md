# API C CVar.GetCVarBool

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the boolean value of a console variable.
 value = C_CVar.GetCVarBool(name)
         {{tlygo|GetCVarBool}}

==Arguments==
:;name:{{apitype|string}} - Name of the CVar to query the value of.

==Returns==
:;value:{{apitype|boolean?}} - Compared to {{api|GetCVar}}, "1" would return as true, "0" would return as false

==Patch changes==
* {{Patch 8.1.5|note=Namespaced to <code>C_CVar.GetCVarBool()</code>.}}
```