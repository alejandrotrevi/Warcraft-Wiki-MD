# API CombatLogGetCurrentEventInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current {{api|t=e|COMBAT_LOG_EVENT}} payload.
 arg1, arg2, ... = CombatLogGetCurrentEventInfo()

==Returns==
* Returns a variable number of values: 11 base values and up to 13 extra values based upon the subtype of the event.

==Details==
* In the new event system for 8.0, supporting the original functionality of the {{api|t=e|COMBAT_LOG_EVENT|CLEU}} event was problematic due to the "context" arguments, i.e. each argument can be interpreted differently depending on the previous arguments. The payload was subsequently moved to this function. <ref>{{ref web|url=http://infobot.rikers.org/%23wowuidev/20180206.html.gz|author=TheDanW|date=2018-02-06|title=#wowuidev IRC log}}</ref>

==Example==
<onlyinclude>* Prints all CLEU parameters.
<syntaxhighlight lang="lua">
local function OnEvent(self, event)
	print(CombatLogGetCurrentEventInfo())
end

local f = CreateFrame("Frame")
f:RegisterEvent("COMBAT_LOG_EVENT_UNFILTERED")
f:SetScript("OnEvent", OnEvent)
</syntaxhighlight>

* Displays your spell or melee critical hits.
<syntaxhighlight lang="lua">
local playerGUID = UnitGUID("player")
local MSG_CRITICAL_HIT = "Your %s critically hit %s for %d damage!"

local f = CreateFrame("Frame")
f:RegisterEvent("COMBAT_LOG_EVENT_UNFILTERED")
f:SetScript("OnEvent", function(self, event)
	local _, subevent, _, sourceGUID, _, _, _, _, destName = CombatLogGetCurrentEventInfo()
	local spellId, amount, critical

	if subevent == "SWING_DAMAGE" then
		amount, _, _, _, _, _, critical = select(12, CombatLogGetCurrentEventInfo())
	elseif subevent == "SPELL_DAMAGE" then
		spellId, _, _, amount, _, _, _, _, _, critical = select(12, CombatLogGetCurrentEventInfo())
	end

	if critical and sourceGUID == playerGUID then
		-- get the link of the spell or the MELEE globalstring
		local action = spellId and GetSpellLink(spellId) or MELEE
		print(MSG_CRITICAL_HIT:format(action, destName, amount))
	end
end)
</syntaxhighlight></onlyinclude>

==Patch changes==
* {{Patch 8.0.1|note=Added. <ref>{{ref web|url=https://us.battle.net/forums/en/wow/topic/20762318007|author=[[Ythisens]]|date=2018-04-24 16:45|title=Combat Log Event Changes}}</ref>}}

==References==

<!-- luals
---@return number timestamp
---@return string subevent
---@return boolean hideCaster
---@return string sourceGUID
---@return string sourceName
---@return number sourceFlags
---@return number sourceRaidFlags
---@return string destGUID
---@return string destName
---@return number destFlags
---@return number destRaidFlags
---@return any ...
function CombatLogGetCurrentEventInfo() end
-->
```