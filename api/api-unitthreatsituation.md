# API UnitThreatSituation

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the threat status of the specified unit to another unit.
 status = UnitThreatSituation(unit [, mobUnit])

==Arguments==
:;unit:{{apitype|UnitToken}} - The player or pet whose threat to request.
:;mobUnit:{{apitype|UnitToken?}} - The NPC whose threat table to query.
::: ''If omitted, returned values reflect whichever NPC unit the player unit has the highest threat against.''

==Returns==
:;status:{{apitype|number?}} - The threat status of the unit on the mobUnit. "High threat" means a unit has 100% threat or higher, "Primary Target" means the unit is the current target of the mob.
<onlyinclude>{| class="sortable darktable zebra col1-center col2-center col3-center" style="margin-left: 3.9em"
|+ style="text-align:left; margin-left: 1em" | {{{caption|}}}
! Value !! High Threat !! Primary Target !! Description
|-
| nil || || || Unit is not on (any) mobUnit's threat table.
|-
| 0 || ❌ || ❌ || Unit has less than 100% threat for mobUnit. The default UI shows no indicator.
|-
| 1 || ✔️ || ❌ || Unit has higher than 100% threat for mobUnit, but isn't the primary target. The default UI shows a yellow indicator.
|-
| 2 || ❌ || ✔️ || Unit is the primary target for mobUnit, but another unit has higher than 100% threat. The default UI shows an orange indicator.
|-
| 3 || ✔️ || ✔️ || Unit is the primary target for mobUnit and no other unit has higher than 100% threat. The default UI shows a red indicator.
|}</onlyinclude>

==Details==
*Threat information for a pair of unit and mobUnit is only returned if the unit has threat against the mobUnit in question. In addition, no threat data is provided if a unit's pet is attacking an NPC but the unit himself has taken no action, even though the pet has threat against the NPC.)<ref>http://wowprogramming.com/docs/api/UnitThreatSituation.html</ref>

==Example==
Prints your threat status for your target if it exists. If the target does not exist or the player is not on the target's threat table, prints your threat status for any other units.
<syntaxhighlight lang="lua">
local statusText = {
	[0] = "(0) low on threat",
	[1] = "(1) high threat",
	[2] = "(2) primary target but not on high threat",
	[3] = "(3) primary target and high threat",
}

local statusTarget = UnitThreatSituation("player", "target")
if UnitExists("target") then
	local msg = statusText[statusTarget] or "not on the target's threat table"
	print("Your threat situation for target unit: "..msg)
end
if not statusTarget then
	-- not in any target unit's threat table, look if on other threat tables
	local statusAny = UnitThreatSituation("player")
	local msg = statusText[statusAny] or "not on any threat table"
	print("Your threat situation for any unit: "..msg)
end

> "Your threat situation for target unit: (3) primary target and high threat"
</syntaxhighlight>

==Patch changes==
====<font color="#4ec9b0">Classic</font>====
* {{Patch 1.13.5|note=Added.<ref name="1.13.5">{{ref web|url=https://us.forums.blizzard.com/en/wow/t/ptr-patch-notes-wow-classic-version-1135/553585|author=[[Kaivax]]|date=2020-06-12|title=PTR Patch Notes - WoW Classic Version 1.13.5}}</ref>}}

==See also==
* {{api|UnitDetailedThreatSituation}}()
* {{api|GetThreatStatusColor}}()

==References==
{{reflist}}
```