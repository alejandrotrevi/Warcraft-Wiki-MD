# API C AddOns.LoadAddOn

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AddOns|system=AddOns}}
Needs summary.
 loaded, value = C_AddOns.LoadAddOn(name)

==Arguments==
:;name:{{apitype|uiAddon}} - The name of the addon to be queried, or an index from 1 to {{api|C_AddOns.GetNumAddOns}}. The state of Blizzard addons can only be queried by name.

==Returns==
:;loaded:{{apitype|boolean?}} - <code>true</code> if the addon was loaded successfully, or if it has already been loaded.
:;value:{{apitype|string?}} - Locale-independent reason why the addon could not be loaded e.g. <code>"DISABLED"</code>, otherwise returns <code>nil</code> if the addon was loaded.

==Details==
* Calling this function inside an {{api|t=e|ADDON_LOADED}} event handler may result in the named addon never receiving its own ADDON_LOADED event, as any new registrations for the event do not take effect until the dispatch of the first event has completed.
```