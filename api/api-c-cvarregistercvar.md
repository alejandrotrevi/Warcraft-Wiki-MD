# API C CVar.RegisterCVar

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Temporarily registers a custom console variable.
 C_CVar.RegisterCVar(name [, value])
        {{tlygo|RegisterCVar}}

==Arguments==
:;name:{{apitype|string}} - Name of the custom CVar to set.
:;value:{{apitype|string,number?|default="0"}} - Initial value of the CVar.

==Details==
* You can register your own CVars. They are set game-wide and will persist after relogging/reloading but not after closing the game.

==Patch changes==
* {{Patch 10.0.7|note=Registered CVars were written to disk, which conflicted with another issue, this was fixed in build 10.0.7.48838.<sup>[https://github.com/Stanzilla/WoWUIBugs/issues/410]</sup>}}
* {{Patch 8.1.5|note=Namespaced to <code>C_CVar.RegisterCVar()</code>.}}
* {{Patch 1.0.0|note=Added.}}
```