# API GetTotemInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Totem}}
Returns info for the specified totem.
 haveTotem, totemName, startTime, duration, icon, modRate, spellID = GetTotemInfo(slot)

==Arguments==
:;slot:{{apitype|number}} - Index of the totem (Fire = 1 Earth = 2 Water = 3 Air = 4)

==Returns==
:;haveTotem:{{apitype|boolean}} - True if you have the totem reagent in your bag ({{Loot|Common|Earth Totem}}, {{Loot|Common|Fire Totem}}, {{Loot|Common|Water Totem}}, {{Loot|Common|Air Totem}}).
:;totemName:{{apitype|string}} - Name of the currently active totem.  If there is no active totem for this slot, this value will apparently be an empty string ("") instead of nil.
:;startTime:{{apitype|number}} - GetTime() value of when the totem started.
:;duration:{{apitype|number}} - Duration (in seconds) of the currently active totem.
:;icon:{{apitype|fileID}} - Path to the icon of the specified totem
:;modRate:{{apitype|number}}
:;spellID:{{apitype|number}}

==Example==
Displays the duration of all active totems
 for index=1,MAX_TOTEMS do
   local arg1, totemName, startTime, duration, icon = GetTotemInfo(index)
   local est_dur = round(startTime+duration-GetTime() )
   DEFAULT_CHAT_FRAME:AddMessage(totemName .. "  " .. est_dur)  
 end

==Details==
* GetTotemTimeLeft(slot): global function returns active time remaining (in seconds) for a totem in a given slot.
* The MAX_TOTEMS constant can be used to determine how many totems are available to iterate over.

==Patch changes==
* {{Patch 11.1.5|note=Added <code>spellID</code> return value.}}
```