# API C CVar.GetCVarBitfield

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the bitfield of a console variable.
 value = C_CVar.GetCVarBitfield(name, index)
       = {{tlygo|GetCVarBitfield}}

==Arguments==
:;name:{{apitype|string}} : [[Console_variables#Console_Variables|CVar]] - name of the CVar.
:;index:{{apitype|number}} - Bitfield index.

==Returns==
:;value:{{apitype|boolean?}} - Value of the bitfield.

==Patch changes==
* {{Patch 8.1.5|note=Namespaced to <code>C_CVar.GetCVarBitfield()</code>.}}

==See also==
* {{api|t=c|closedInfoFrames}}
```