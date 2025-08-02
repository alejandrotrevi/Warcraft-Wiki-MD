# API GetMacroSpell

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the spell a given macro is set to cast. 
 id = GetMacroSpell(name)

==Arguments==
:;name:{{apitype|number,string}} - The macro index to query, or the name of the macro to query.

==Returns==
:;id:{{apitype|number}} - The ability's spellId.

==Details==
* Action-bar addons use this function to display dynamic macro icons, tooltips and glow effects.  As a macro's cast sequence changes, this function indicates which will be cast next.

==Example==
<syntaxhighlight lang="lua">
local macroName = "MyMacro"
local index = GetMacroIndexByName(macroName)
if index then 
	local spellId = GetMacroSpell(index)
	if spellId then
		print(macroName .. " will now cast " .. GetSpellLink(spellId))
	end
end
</syntaxhighlight>

==Patch changes==
* {{Patch 8.0.1|note=Removed original two return values, name and rank.<ref>{{ref web|author={{Blizz}}[[Aerythlea]]|title=Battle for Azeroth Addon Changes|date=2018-11-14|url=https://eu.forums.blizzard.com/en/wow/t/battle-for-azeroth-addon-changes/1643}}</ref><ref>{{ref FrameXML|ActionButton.lua|8.0.1|27101|643|2018-07-16}}</ref>}}
* {{Patch 4.3.0|note=Added third return value, id.<ref>{{ref FrameXML|ActionButton.lua|4.3.0|15005|414|2011-11-15}}</ref>}}
* {{Patch 2.3.0|note=Added.<ref>{{ref web|author={{Blizz}}[[slouken]]|title=Re: Upcoming 2.3 Changes - Concise List|url=http://forums.worldofwarcraft.com/thread.html?topicId=879058320&pageNo=1&sid=1#18|archiveurl=http://blue.cardplace.com/newcache/us/879058320.htm|date=2007-08-27}}</ref>}}

==References==
{{Reflist}}
```