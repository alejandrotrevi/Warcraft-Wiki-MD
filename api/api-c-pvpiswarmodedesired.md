# API C PvP.IsWarModeDesired

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Indicates whether the player has opted into [[War Mode]] beginning with ''Battle for Azeroth'', regardless if the player is in an outdoor zone where such PvP is actually possible.
 warModeDesired = C_PvP.IsWarModeDesired()

==Returns==
:;warModeDesired:{{apitype|boolean}} - True if the player has turned war mode on; false otherwise.

==Example==
The following example is adpated from <code>FrameXML/PartyMemberFrame.lua</code><sup>[https://www.townlong-yak.com/framexml/live/PartyMemberFrame.lua]</sup>
<syntaxhighlight lang="lua">
for i=1, 4                                  
	local unit = "party"..i
	if UnitExists(unit) then                   
		if UnitInPhase(unit) then                
			print(string.format("Party member %d: Currently in phase!", i))
		else
			if UnitIsWarModePhased(unit) then
				if C_PvP.IsWarModeDesired() then    
					print(string.format("Party member &d: %s",i, PARTY_PLAYER_WARMODE_DISABLED))
				else
					print(string.format("Party member &d: %s",i, PARTY_PLAYER_WARMODE_ENABLED))
				end
			else
				print(string.format("Party member &d: %s",i, PARTY_PHASED_MESSAGE))
			end
		end
	end
end
</syntaxhighlight>
==Patch changes==
* {{Patch 8.0.1|note=Added.}}

==See also==
* {{api|GetPVPDesired()}}
```