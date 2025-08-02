# API C FunctionContainers.CreateCallback

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Creates a function container that invokes a cancellable callback function.
 container = C_FunctionContainers.CreateCallback(func)

==Arguments==
:;func:{{apitype|function}} - A Lua function to be called.

==Returns==
:;container:{{apitype|FunctionContainer}} - A container object ({{apitype|userdata}}) bound to the supplied function.

==Details==
* The supplied callback must be a Lua function. The API will reject C functions and any non-function values.

==Example==
The following snippet creates a function container and schedules it to be executed every second, cancelling itself after five calls.
<syntaxhighlight lang="lua">
local container
container = C_FunctionContainers.CreateCallback(function()
    container.timesCalled = container.timesCalled + 1

    if container.timesCalled == 5 then
        container:Cancel()
    end

    print("Called!")
end)

container.timesCalled = 0
C_Timer.NewTicker(1, container)
</syntaxhighlight>

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```