# API C CVar.SetCVarBitfield

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the bitfield of a console variable.
 success = C_CVar.SetCVarBitfield(name, index, value)
         = {{tlygo|SetCVarBitfield}}

==Arguments==
:;name:{{apitype|string}} - Name of the CVar to set the bitfield of.
:;index:{{apitype|number}} - Bitfield index.
:;value:{{apitype|boolean}} - The new value of the bitfield.

==Returns==
:;success:{{apitype|boolean}} - Whether the CVar was successfully set.

==Patch changes==
* {{Patch 10.0.0|note=Removed <code>scriptCVar</code> argument.}}
* {{Patch 8.1.5|note=Nanespaced to <code>C_CVar.SetCVarBitfield()</code>.}}

==See also==
* {{api|t=c|closedInfoFrames}}
```