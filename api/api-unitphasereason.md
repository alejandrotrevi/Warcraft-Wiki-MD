# API UnitPhaseReason

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the reason if a unit is NOT in the same phase.
 reason = UnitPhaseReason(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;reason:{{apitype|Enum.PhaseReason?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| align="center" | 0 || Phasing || The unit is in a different [[Phasing|phase]]
|-
| align="center" | 1 || Sharding || The unit is in a different [[Sharding (term)|shard]]
|-
| align="center" | 2 || WarMode || The unit has a different [[war mode]]
|-
| align="center" | 3 || ChromieTime || The unit is in a [[Timewalking Campaign]]
|}

==Details==
* Returns <code>nil</code> if the unit is in the same phase.

==Example==
<syntaxhighlight lang="lua">
local function PrintPhaseReason(unit)
	local msg
	local reason = UnitPhaseReason(unit)
	if reason == Enum.PhaseReason.WarMode then
		msg = "has a different warmode"
	elseif reason == Enum.PhaseReason.ChromieTime then
		msg = "either of you is doing a Timewalking Campaign"
	elseif reason == Enum.PhaseReason.Phasing then
		msg = "is in a different phase"
	elseif reason == Enum.PhaseReason.Sharding then
		msg = "is in a different shard"
	elseif not reason then
		msg = "is in the same phase"
	end
	print(unit, msg)
end

PrintPhaseReason("party1")
</syntaxhighlight>

==Patch changes==
* {{Patch 9.0.1|note=Added. Replaces {{api|UnitIsWarModePhased}}() and {{api|t=a|UnitInPhase}}() }}

==See also==
* {{api|t=e|UNIT_PHASE}}
```