# API IsAddOnLoadOnDemand

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.0|removed=11.0.2}}
Returns true if the specified addon is load-on-demand.
 loadDemand = IsAddOnLoadOnDemand(name)

==Arguments==
{{:AddOnInfo}}

==Returns==
:;loadDemand:{{apitype|boolean}} - True if the specified addon is loaded on demand.

==Example==
Loads every LoD addon.
 for i = 1, GetNumAddOns() do
     if IsAddOnLoadOnDemand(i) then
         LoadAddOn(i)
     end
 end

{{apinavbox|AddOn}}
```