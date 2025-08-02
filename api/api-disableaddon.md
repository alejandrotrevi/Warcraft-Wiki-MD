# API DisableAddOn

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.0|removed=11.0.2}}
Disables an addon for subsequent sessions.
 DisableAddOn(addon [, character])

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
* Attempting to disable secure addons with the GuardedAddOn [[TOC format#Restricted|TOC metadata field]] will result in an "Cannot disable a guarded AddOn" error.

==Example==
{{:API_EnableAddOn}}

==Patch changes==
* {{Patch 11.0.2|note=Removed, replaced by {{api|C_AddOns.DisableAddOn}}.}}
* {{Patch 10.1.0|note=Secure addons with the GuardedAddOn TOC metadata field can no longer be disabled.}}

{{apinavbox|AddOn}}
```