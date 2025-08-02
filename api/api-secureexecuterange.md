# API secureexecuterange

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Calls a function for each pair within a table without propagating taint to the caller.
 secureexecuterange(tbl, func, ...)

==Arguments==
:;tbl:{{apitype|table}} - The table to be traversed.
:;func:{{apitype|function}} - The function to be called for each pair.
:;...:Additional arguments to supply to the invoked function.

==Details==

* The supplied function will be called with the key and value of each pair within the table as the first two arguments, followed by any additional user-supplied arguments.
* Execution of the supplied function will be tainted in the following scenarios:
** If the initial state of execution was insecure.
** If the table pair currently being processed was insecurely inserted.
** If the supplied function was created by insecure code.
* If execution is tainted during the processing of a single pair, the taint does not propagate to the processing of any remaining pairs within the supplied table.
* Errors that occur during the execution of the supplied function are discarded, and do not propagate to the caller. Additionally, errors do not prevent the function from being called for all remaining pairs within the supplied table so as to prevent insecure code from potentially changing the flow of execution.

===Example Implementation===

The implementation of this function would, if not provided natively by the client, be effectively similar to the snippet below. This example aims to demonstrate how error handling and taint is processed with regards to individual pairs within the table.

<syntaxhighlight lang="lua">
local function secureexecutenext(tbl, prev, func, ...)
    local key, value = next(tbl, prev)

    if key ~= nil then
        pcall(func, key, value, ...)  -- Errors are silently discarded!
    end

    return key
end

function secureexecuterange(tbl, func, ...)
    local key = nil

    repeat
        key = securecallfunction(secureexecutenext, tbl, key, func, ...)
    until key == nil
end
</syntaxhighlight>

==Patch changes==
* {{Patch 9.1.5|note=Added.}}

{{API Trail Secure}}
<!-- luals
---@param tbl table
---@param func function
---@param ... any
function secureexecuterange(tbl, func, ...) end
-->
```