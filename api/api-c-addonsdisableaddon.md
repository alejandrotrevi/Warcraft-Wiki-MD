# API C AddOns.DisableAddOn

**Contributor:** Ghostopheles

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AddOns|system=AddOns}}
Sets an addon to be disabled.
 C_AddOns.DisableAddOn(name [, character])

==Arguments==
:;name:{{apitype|uiAddon}} - The name of the addon to be disabled, or an index from 1 to {{api|C_AddOns.GetNumAddOns}}. Blizzard addons cannot be disabled.
:;character:{{apitype|string?}} - The name or [[GUID]] of the character, excluding the realm name. If omitted, disables the addon for all characters.

==Details==
: The addon will be disabled on the next session, when reloading or relogging.

==Example==
Disables an addon for all characters on the current realm.
<syntaxhighlight lang="lua">
C_AddOns.DisableAddOn("HelloWorld")
</syntaxhighlight>

Disables an addon only for the current character.
<syntaxhighlight lang="lua">
C_AddOns.DisableAddOn("HelloWorld", UnitName("player"))
</syntaxhighlight>

==Patch changes==
* {{Hotfix|date=2024-05-16|version=10.2.7.54736|note=This function can no longer be used to disable secure Blizzard addons.|doc=}}
* {{Patch 10.2.0|note=Namespaced to <code>C_AddOns</code>. This now defaults to all characters instead of the current character if the <code>character</code> param is omitted.}}
```