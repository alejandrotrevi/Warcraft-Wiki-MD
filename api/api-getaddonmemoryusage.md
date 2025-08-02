# API GetAddOnMemoryUsage

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the memory used for an addon.
 mem = GetAddOnMemoryUsage(name)

==Arguments==
{{:AddOnInfo}}

==Returns==
:;mem:{{apitype|number}} - Memory usage of the addon in kilobytes.

==Details==
* This function returns a cached value calculated by {{api|UpdateAddOnMemoryUsage}}()
* This function will raise an error if a secure Blizzard addon is queried.

==Example==
Prints the memory usage for all addons.
<syntaxhighlight lang="lua">
UpdateAddOnMemoryUsage()
for i = 1, GetNumAddOns() do
	local name = GetAddOnInfo(i)
	print(GetAddOnMemoryUsage(i), name)
end
</syntaxhighlight>

==Patch changes==
* {{Patch 10.1.0|note=Will now raise an error if a secure addon is queried.}}
```