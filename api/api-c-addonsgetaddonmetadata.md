# API C AddOns.GetAddOnMetadata

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AddOns|system=System}}
Returns the TOC metadata of an addon.
 value = C_AddOns.GetAddOnMetadata(name, variable)

==Arguments==
:;name:{{apitype|uiAddon}} - The name or index of the addon, case insensitive.
:;variable:{{apitype|string}} - Variable name, case insensitive. May be <code>Title, Notes, Author, Version</code>, or anything starting with <code>X-</code>

==Returns==
:;value:{{apitype|string?}} - The value of the variable, <code>nil</code> if not defined.

==Details==
* Unlike {{api|GetAddOnMetadata}}, this function will raise an "Invalid AddOn name" error if supplied the name of an addon that does not exist.

{{apinavbox|AddOn}}{{apinavbox|Authoring}}
```