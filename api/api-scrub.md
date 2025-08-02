# API scrub

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the argument list with non-number/boolean/string values changed to nil.
 ... = scrub(...)

==Arguments==
:;...:{{apitype|any}} - The values to be scrubbed.

==Returns==
:;...:{{apitype|boolean,number,string,nil}} - The scrubbed list of arguments.

==Patch changes==
* {{Patch 2.0.1|note=Added.}}
<!-- luals
---@param ... any
---@return string|boolean|number|nil ...
function scrub(...) end
-->
```