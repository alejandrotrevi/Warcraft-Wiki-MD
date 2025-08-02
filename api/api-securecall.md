# API securecall

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Calls the specified function without propagating taint to the caller.
 ... = securecall(func or functionName, ...)
 ... = securecallfunction(func, ...)

==Arguments==
:;func:{{apitype|function,string}} - A direct reference of the function to be called, or for <code>securecall</code> a string name of a function to be resolved through a global lookup.
:;...:Additional arguments to supply to the function.

==Returns==
:;...:The return values of the called function.

==Details==
* If <code>securecall</code> is called from a [[Secure Execution and Tainting|secure execution path]], the execution path will remain secure when <code>securecall</code> returns, even if the called function is tainted, or accesses tainted variables.
* Errors that occur within the called function are not propagated to the caller; if an error occurs, <code>securecall</code> triggers the {{api|geterrorhandler|default error handler}}, and then returns control to the caller with no return values.
* For <code>securecallfunction</code>, no attempt is made to perform a global lookup based on the supplied function argument.

==Patch changes==
* {{Patch 9.1.5|note=Added <code>securecallfunction</code>.}}
* {{Patch 2.0.1|note=Added <code>securecall</code>.}}

{{API Trail Secure}}
<!-- luals
---@generic A, R
---@generic S : string
---@param funcOrKey S|fun(...: A): ...:R
---@param ... A
---@return R ...
function securecall(funcOrKey, ...) end

---[Documentation](https://warcraft.wiki.gg/wiki/API_securecallfunction)
---@generic A, R
---@param func fun(...: A): ...:R
---@param ... A
---@return R ...
function securecallfunction(func, ...) end
-->
```