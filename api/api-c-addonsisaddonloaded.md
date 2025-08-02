# API C AddOns.IsAddOnLoaded

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AddOns|system=AddOns}}
Needs summary.
 loadedOrLoading, loaded = C_AddOns.IsAddOnLoaded(name)

==Arguments==
:;name:{{apitype|uiAddon}} - The name of the addon to be queried, or an index from 1 to {{api|C_AddOns.GetNumAddOns}}. The state of Blizzard addons can only be queried by name.

==Returns==
:;loadedOrLoading:{{apitype|boolean}}
:;loaded:{{apitype|boolean}}
```