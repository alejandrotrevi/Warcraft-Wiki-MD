# API pcallwithenv

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Calls a function in protected mode with a temporarily replaced function environment.
 ok, ... = pcallwithenv(func, env, ...)

==Arguments==
:;func:{{apitype|string}} - The function to be called.
:;env:{{apitype|table}} - A custom environment table to apply to the function prior to calling.
:;...:Variable - Arguments to supply to the function.

==Returns==
:;ok:{{apitype|boolean}} - True if the function was called without error.
:;...:Variable - Either a singular error value or all of the return values of the called function.

==Details==
* This function will temporarily replace the existing environment on the supplied function before the call, and will restore the original environment after the call has completed.
* This function will raise an error if the function to be called has an existing environment whose metatable has an __environment field set.
* If this function is called insecurely and the supplied function is a Lua function, the supplied function will be irrevocably tainted. This will result in all future calls to the function tainting execution.

==Patch changes==
* {{Patch 10.1.0|note=Added.}}

==See also==
* {{api|pcall}}
* {{api|setfenv}}
```