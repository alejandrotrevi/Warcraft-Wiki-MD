# API C AddOns.GetAddOnOptionalDependencies

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AddOns|system=AddOns}}
Returns a list of optional TOC dependencies.
 dep1, ... = C_AddOns.GetAddOnOptionalDependencies(name)

==Arguments==
:;name:{{apitype|uiAddon}} - The name of the addon to be queried, or an index from 1 to {{api|C_AddOns.GetNumAddOns}}. The state of Blizzard addons can only be queried by name.

==Returns==
:;dep1, ...:{{apitype|string?}} - A list of addon names that are an optional dependency.
```