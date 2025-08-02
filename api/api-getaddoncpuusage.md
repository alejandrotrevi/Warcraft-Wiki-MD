# API GetAddOnCPUUsage

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the total time used for an addon.
 time = GetAddOnCPUUsage(name)

==Arguments==
{{:AddOnInfo}}

==Returns==
:;time:{{apitype|number}} - The total time used by the specified AddOn, in milliseconds.

==Details==
* This function will raise an error if a secure Blizzard addon is queried.
* This function returns a cached value calculated by UpdateAddOnCPUUsage(). The time is the sum of GetFunctionCPUUsage(f, false) for all functions f created on behalf of the AddOn. These functions include both functions created directly by the AddOn itself, as well as functions created by external functions that where called by the AddOn. That means even though an external function does not belong to an AddOn, functions created by that external function are attributed to the calling AddOn.

* Notably, the time used does NOT include calls into the WoW API.
: Running this code will show the addon using 300-350ms CPU time:
  e=debugprofilestop()+500; while debugprofilestop()<e do end
  -- we're spending a lot of time simply calling the API!
: But running THIS code will show the addon using much closer to 500ms CPU time:
  e=debugprofilestop()+500; while debugprofilestop()<e do 
    for i=1,1000 do end
  end
: However, in both cases, :GetFrameCPUUsage() on the addon's frame will report 500ms used.

==Patch changes==
* {{Patch 10.1.0|note=Will now raise an error if a secure addon is queried.}}

<!-- luals
---@param name number|string
---@return number time
function GetAddOnCPUUsage(name) end
-->
```