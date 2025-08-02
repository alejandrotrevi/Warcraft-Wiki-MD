# API GetBinding

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name and keys for a binding by index.
 command, category, key1, key2, ... = GetBinding(index [, alwaysIncludeGamepad])

==Arguments==
:;index:{{apitype|number}} - index of the binding to query, from 1 to [[API GetNumBindings|GetNumBindings]]().
:;alwaysIncludeGamepad:{{apitype|boolean?}} - If gamepad support is disabled, then gamepad bindings are only returned if this is <code>true</code>.

==Returns==
:;command:{{apitype|string}} - Command this binding will perform (e.g. MOVEFORWARD). For well-behaved bindings, a human-readable description is stored in the <code>_G["BINDING_NAME_" .. command]</code> global variable.
:;category:{{apitype|string}} - Category this binding was declared in (e.g. BINDING_HEADER_MOVEMENT). For well-behaved bindings, a human-readable title is stored in the <code>_G[category]</code> global variable.
:;key1, key2, ...:{{apitype|string?}} - Key combination this binding is bound to (e.g. W, CTRL-F). <code>key1</code> and <code>key2</code> can be nil if there is nothing bound to the command.

==Details==
* Even though the default Key Binding window only shows up to two bindings for each command, it is actually possible to bind more using [[API SetBinding|SetBinding]], and this function will return all of the keys bound to the given command, not just the first two.

==Example==
<syntaxhighlight lang="lua">
local function dumpBinding(command, category, ...)
	local cmdName = _G["BINDING_NAME_" .. command]
	local catName = _G[category]
	print(("%s > %s (%s) is bound to:"):format(catName or "?", cmdName or "?", command), strjoin(", ", ...))
end

dumpBinding(GetBinding(5)) -- "Movement Keys > Turn Right (TURNRIGHT) is bound to: D, RIGHT"
</syntaxhighlight>

==See also==
* [[API GetBindingAction|GetBindingAction]]
* [[API GetBindingKey|GetBindingKey]]
* [[API GetBindingByKey|GetBindingByKey]]
* [[Bindings.xml]]
<!-- luals
---@param index number
---@param alwaysIncludeGamepad? boolean
---@return string command
---@return string category
---@return string? key1
---@return string? key2
---@return string? ...
function GetBinding(index, alwaysIncludeGamepad) end
-->
```