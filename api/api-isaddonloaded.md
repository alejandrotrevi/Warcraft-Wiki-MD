# API IsAddOnLoaded

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.0|removed=11.0.2}}
Returns true if the specified addon is loaded.
 loaded, finished = IsAddOnLoaded(name)

==Arguments==
{{:AddOnInfo}}

==Returns==
:;loaded:{{apitype|boolean}} - True if the addon has been, or is being loaded.
:;finished:{{apitype|boolean}} - True if the addon has finished loading and {{api|t=e|ADDON_LOADED}} has been fired for this addon.

{{apinavbox|AddOn}}
```