# API UnitGUID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the GUID of the unit.
 guid = UnitGUID(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - For example <code>"player"</code> or <code>"target"</code>

==Returns==
:;guid:{{apitype|string?}} : [[GUID#Creature|GUID]] - A string containing (hexadecimal) values, delimited with hyphens. Returns <code>nil</code> if the unit does not exist.

==Example==
Prints the target's GUID, in this case a creature.
<syntaxhighlight lang="lua">
/dump UnitName("target"), UnitGUID("target")
> "Hogger", "Creature-0-1465-0-2105-448-000043F59F"
</syntaxhighlight>

Prints the npc/player ID of a unit, if applicable.
<syntaxhighlight lang="lua">
local unitLink = "|cffffff00|Hunit:%s|h[%s]|h|r"

local function ParseGUID(unit)
	local guid = UnitGUID(unit)
	local name = UnitName(unit)
	if guid then
		local link = unitLink:format(guid, name) -- clickable link
		local unit_type = strsplit("-", guid)
		if unit_type == "Creature" or unit_type == "Vehicle" then
			local _, _, server_id, instance_id, zone_uid, npc_id, spawn_uid = strsplit("-", guid)
			print(format("%s is a creature with NPC ID %d", link, npc_id))
		elseif unit_type == "Player" then
			local _, server_id, player_id = strsplit("-", guid)
			print(format("%s is a player with ID %s", link, player_id))
		end
	end
end
</syntaxhighlight>

==See also==
* {{api|GetPlayerInfoByGUID}}()

==Patch changes==
* {{Patch 2.4.0|note=Added.}}
```