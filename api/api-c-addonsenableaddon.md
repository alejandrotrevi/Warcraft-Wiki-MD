# API C AddOns.EnableAddOn

**Contributor:** Ghostopheles

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AddOns|system=AddOns}}
Sets an addon to be enabled.
 C_AddOns.EnableAddOn(name [, character])

==Arguments==
:;name:{{apitype|uiAddon}} - The name of the addon to be enabled, or an index from 1 to {{api|C_AddOns.GetNumAddOns}}. Blizzard addons can only be enabled by name.
:;character:{{apitype|string?}} - The name or [[GUID]] of the character, excluding the realm name. If omitted, enables the addon for all characters.

==Details==
: The addon will be enabled on the next session, when reloading or relogging.

==Example==
Enables an addon for all characters on the current realm.
<syntaxhighlight lang="lua">
C_AddOns.EnableAddOn("HelloWorld")
</syntaxhighlight>

Enables an addon only for the current character.
<syntaxhighlight lang="lua">
C_AddOns.EnableAddOn("HelloWorld", UnitName("player"))
</syntaxhighlight>

==Patch changes==
* {{Patch 10.2.0|note=Namespaced to <code>C_AddOns</code>. This now defaults to all characters instead of the current character if the <code>character</code> param is omitted.}}
```