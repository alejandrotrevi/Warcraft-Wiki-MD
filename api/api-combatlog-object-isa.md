# API CombatLog Object IsA

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether a unit from the combat log matches a given filter.
 isMatch = CombatLog_Object_IsA(unitFlags, mask)

==Arguments==
:;unitFlags:{{apitype|number}} - [[UnitFlag]] bitfield, i.e. <code>sourceFlags</code> or <code>destFlags</code> from {{api|t=e|COMBAT_LOG_EVENT}}.
:;mask:{{apitype|number}} - [https://github.com/Gethe/wow-ui-source/blob/9.2.0/Interface/FrameXML/Constants.lua#L291 COMBATLOG_FILTER] constant.

==Returns==
:;isMatch:{{apitype|boolean}} - True if a bitfield in each of the four main categories matches.

==Details==
* Both of the arguments to this function must be valid Combat Log Objects. That is, for the four main categories of the [[UnitFlag]] bitfield, there must be at least one nonzero bit. Passing in a single COMBATLOG_OBJECT constant will cause the check to return false.

==Filters==
{| class="darktable zebra"
! Constant !! colspan="9" | bit field
|-
| COMBATLOG_FILTER_ME || 0x||0||0||0||0||0||5||1||1
|-
| COMBATLOG_FILTER_MINE || 0x||0||0||0||0||4||5||1||1
|-
| COMBATLOG_FILTER_MY_PET || 0x||0||0||0||0||3||1||1||1
|-
| COMBATLOG_FILTER_FRIENDLY_UNITS || 0x||0||0||0||0||7||F||1||E
|-
| COMBATLOG_FILTER_HOSTILE_PLAYERS || 0x||0||0||0||0||7||D||4||E
|-
| COMBATLOG_FILTER_HOSTILE_UNITS || 0x||0||0||0||0||7||E||4||E
|-
| COMBATLOG_FILTER_NEUTRAL_UNITS || 0x||0||0||0||0||7||F||2||E
|-
| COMBATLOG_FILTER_UNKNOWN_UNITS || 0x||8||0||0||0||0||0||0||0
|-
| COMBATLOG_FILTER_EVERYTHING || 0x||F||F||F||F||F||F||F||F
|}

You can also construct your own filter; make sure to use at least one constant from each category:
<syntaxhighlight lang="lua">
local COMBATLOG_FILTER_FRIENDLY_PLAYERS = bit.bor(
	COMBATLOG_OBJECT_AFFILIATION_PARTY,
	COMBATLOG_OBJECT_AFFILIATION_RAID,
	COMBATLOG_OBJECT_AFFILIATION_OUTSIDER,
	COMBATLOG_OBJECT_REACTION_FRIENDLY,
	COMBATLOG_OBJECT_CONTROL_PLAYER,
	COMBATLOG_OBJECT_TYPE_PLAYER
)
</syntaxhighlight>

==Example==
<onlyinclude>Prints if the combat log source unit is a hostile NPC.
<syntaxhighlight lang="lua">
local f = CreateFrame("Frame")
f:RegisterEvent("COMBAT_LOG_EVENT_UNFILTERED")
f:SetScript("OnEvent", function(self, event)
	local timestamp, subevent, _, sourceGUID, sourceName, sourceFlags = CombatLogGetCurrentEventInfo()
	if CombatLog_Object_IsA(sourceFlags, COMBATLOG_FILTER_HOSTILE_UNITS) then
		print(subevent, sourceName, format("0x%X", sourceFlags), "is a hostile NPC")
	end
end)
</syntaxhighlight></onlyinclude>

==Patch changes==
* {{Patch 2.4.2|note=Added.}}
```