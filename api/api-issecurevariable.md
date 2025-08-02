# API issecurevariable

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the specified variable is secure.
 isSecure, taint = issecurevariable([tbl,] variable)

==Arguments==
:;tbl:{{apitype|table?}} - table to check the the key in; if omitted, defaults to the globals table (<code>_G</code>).
:;variable:{{apitype|string}} - string key to check the taint of. Numbers will be converted to a string; other types will throw an error.

==Returns==
:;isSecure:{{apitype|boolean}} - true if the <code>table[variable]</code> key is secure, false if it is tainted.
:;taint:{{apitype|string?}} - name of the addon that tainted the table field; an empty string if tainted by a macro; nil if secure.

==Details==
* Also returns <code>true, nil</code> for keys that have never been used/defined, because nothing has tainted them yet.
* If <code>table[variable] == nil</code>, and table has a metatable with <code>__index</code>, this function will return whether the metatable's <code>__index[varible]</code> is tainted. You must remove the metatable to check whether <code>table[variable]</code> itself is tainted.
* Cannot be used to check taint of local variables, or non-string table keys.



{{API Trail Secure}}
<!-- luals
---@param tbl table
---@param variable string
---@return boolean isSecure
---@return string? taint
---@overload fun(variable: string)
function issecurevariable(tbl, variable) end
-->
```