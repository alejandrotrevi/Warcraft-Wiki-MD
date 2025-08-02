# API GetAddOnMetadata

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.1.0|removed=11.0.2}}
Returns the TOC metadata of an addon.
 value = GetAddOnMetadata(index, field)
         GetAddOnMetadata(name, field)

==Arguments==
:;index:{{apitype|index}} - The index in the addon list. Note that you cannot query Blizzard addons by index.
:;name:{{apitype|string}} - The name of the addon, case insensitive.
:;field:{{apitype|string}} - Field name, case insensitive. May be Title, Notes, Author, Version, or anything starting with X-

==Returns==
:;value:{{apitype|string?}} - The value of the field.

<!-- luals
---@param index number
---@param field string
---@return string? value
---@overload fun(name: string, field: string)
function GetAddOnMetadata(index, field) end
-->
```