# API EnableAddOn

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.0|removed=11.0.2}}
Enables an addon for subsequent sessions.
 EnableAddOn(addon [, character])

==Arguments==
:;addon
::{{apitype|number}} - <code>addonIndex</code> from 1 to {{api|t=a|GetNumAddOns}}()
::''or'' {{apitype|string}} - <code>addonName</code> (as in toc/folder filename) of the addon, case insensitive.
:;character
::{{apitype|string?}} - <code>playerName</code> of the character (without realm)
::''or'' {{apitype|boolean?}} - <code>enableAll</code> True if the addon should be enabled/disabled for all characters on the realm.
::: Defaults to the current character. <s>This param is currently bugged when attempting to use it ([https://github.com/Stanzilla/WoWUIBugs/issues/156 Issue #156]).</s>

==Details==
* Takes effect only after [[API_ReloadUI|reloading]] the UI.

==Example==
<onlyinclude>* Enables the addon at index 1 for the current character.
<syntaxhighlight lang="lua">
function PrintAddonInfo(idx)
	local name = GetAddOnInfo(idx)
	local enabledState = GetAddOnEnableState(nil, idx)
	print(name, enabledState)
end

PrintAddonInfo(1) -- "HelloWorld", 0
EnableAddOn(1)
PrintAddonInfo(1) -- "HelloWorld", 2
</syntaxhighlight>

* This should enable an addon for all characters, provided it isn't bugged.
<syntaxhighlight lang="lua">
EnableAddOn("HelloWorld", true)
</syntaxhighlight>

* Blizzard addons can be only accessed by name instead of index.
<syntaxhighlight lang="lua">
DisableAddOn("Blizzard_CombatLog")
</syntaxhighlight></onlyinclude>

{{apinavbox|AddOn}}
```