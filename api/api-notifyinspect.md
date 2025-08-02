# API NotifyInspect

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Requests another player's inventory and talent info before inspecting.
 NotifyInspect(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit to inspect.

==Details==
* Triggers {{api|t=e|INSPECT_READY}} when information is asynchronously available.
* Requires an eligible unit within range, confirmed with {{api|CanInspect}}() and {{api|CheckInteractDistance}}().
* The client continues checking equipment and talent changes until halted by {{api|ClearInspectPlayer}}().

==Patch changes==
* {{Patch 3.3.5|note=The server may throttle the amount of requests; no event fires when this happens.}}

==See also==
* {{api|RequestInspectHonorData}}() - Classic only function for PvP statistics.
```