# API UnitAura

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.5|removed=11.0.2}} {{tocright}}
Returns the buffs/debuffs for the unit.
 name, icon, count, dispelType, duration, expirationTime, source, isStealable, nameplateShowPersonal,
 spellId, canApplyAura, isBossDebuff, castByPlayer, nameplateShowAll, timeMod, ...
     = UnitAura  (unit, index [, filter])
     = UnitBuff  (unit, index [, filter])
     = UnitDebuff(unit, index [, filter])

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]
:;index:{{apitype|number}} - Index of an aura to query.
:;filter:{{apitype|string?}} - A list of filters, separated by pipe chars or spaces. Otherwise defaults to "HELPFUL".

==Filters==
* UnitBuff() is an alias for <code>UnitAura(unit, index, "HELPFUL")</code>, returning only buffs.
* UnitDebuff() is an alias for <code>UnitAura(unit, index, "HARMFUL")</code>, returning only debuffs.
{{:AuraFilter}}

==Returns==
: Returns <code>nil</code> when there is no aura for that index or when the aura doesn't pass the filter.
<onlyinclude>{{AuraType|aura}}</onlyinclude>

==Details==
* UnitBuff() will ignore any HARMFUL filter, and vice versa UnitDebuff() will ignore any HELPFUL filter.
* Filters can be mutually exclusive, e.g. <code>"HELPFUL|HARMFUL"</code> will always return nothing.
* On retail a unit can have an unlimited amount of buffs/debuffs.
:* {{Wow-inline}} The [[debuff]] limit is at 16 for Classic Era and 40 for BCC.
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|UNIT_AURA}} }}
|}

===World Buffs===
{{wow-inline}} If the unit has the [[Supercharged Chronoboon Displacer]] buff, then the world buffs can be selected from the return values. For example for [[Warchief's Blessing]]:
<syntaxhighlight lang="lua">
select(20, UnitBuff("player", index))
</syntaxhighlight>
{| class="darktable zebra"
! Buff !! Type !! Description
|-
| 17. [[Fengus' Ferocity]] || style="padding-right: 1em" | {{apitype|number}} || Duration
|-
| 18. [[Mol'dar's Moxie]] || {{apitype|number}} || Duration 
|-
| 19. [[Slip'kik's Savvy]] || {{apitype|number}} || Duration 
|-
| 20. [[:Rallying Cry of the Dragonslayer]] || {{apitype|number}} || Duration 
|-
| 21. [[:Warchief's Blessing]] || {{apitype|number}} || Duration 
|-
| 22. [[:Spirit of Zandalar]] || {{apitype|number}} || Duration 
|-
| 23. [[:Songflower Serenade]] || {{apitype|number}} || Duration 
|-
| 24. [[Sayge's Fortune]] || {{apitype|number}} || Duration of the chosen buff
|-
| 25. [[Sayge's Fortune]] || {{apitype|number}} || spellID of the chosen buff
|-
| 26. [[Boon of Blackfathom]] || {{apitype|number}} || Duration 
|-
| 27. [[Spark of Inspiration]] || {{apitype|number}} || Duration 
|-
| 28. [[Fervor of the Temple Explorer]] || {{apitype|number}} || Duration 
|}

==Example==
* Prints the third aura on the target.
<syntaxhighlight lang="lua">
/dump UnitAura("target", 3)

[1] = "Power Word: Fortitude", -- name
[2] = 135987,     -- icon
[3] = 0,          -- count
[4] = "Magic",    -- dispelType
[5] = 3600,       -- duration
[6] = 112994.871, -- expirationTime 
[7] = "player",   -- source
[8] = false,      -- isStealable
[9] = false,      -- nameplateShowPersonal
[10] = 21562,     -- spellID
[11] = true,      -- canApplyAura
[12] = false,     -- isBossDebuff
[13] = true,      -- castByPlayer
[14] = false,     -- nameplateShowAll
[15] = 1,         -- timeMod
[16] = 5,         -- attribute1: Stamina increased by 5%
[17] = 0          -- attribute2: Magic damage taken reduced by 0% (Thorghast Enchanted Shroud power)
</syntaxhighlight>

* The following are equivalent. Prints the first debuff applied by the player on the target.
 /dump UnitAura("target", 1, "PLAYER|HARMFUL")
 /dump UnitDebuff("target", 1, "PLAYER")

* {{api|GetPlayerAuraBySpellID}}() is useful for checking only a specific aura on the player character.
 /dump GetPlayerAuraBySpellID(21562)

==Aura Util==
===ForEachAura===
 [https://github.com/Gethe/wow-ui-source/search?q=ForEachAura AuraUtil.ForEachAura]<code>(unit, filter, [maxCount], func, [usePackedAura])</code>
This is recommended for iterating over auras. For example to print all buffs:
<syntaxhighlight lang="lua">
AuraUtil.ForEachAura("player", "HELPFUL", nil, function(name, icon, ...)
	print(name, icon, ...)
end)
</syntaxhighlight>

The callback function should return <code>true</code> once it's fine to stop processing further auras.
<syntaxhighlight lang="lua">
local function foo(name, icon, _, _, _, _, _, _, _, spellId, ...)
	if spellId == 21562 then -- Power Word: Fortitude
		-- do stuff
		return true
	end
end
AuraUtil.ForEachAura("player", "HELPFUL", nil, foo)
</syntaxhighlight>

===FindAuraByName===
 [https://github.com/Gethe/wow-ui-source/search?q=FindAuraByName AuraUtil.FindAuraByName]<code>(name, unit [, filter])</code>
Finds the ''first'' aura that matches the name, but note that:
* Aura names are not unique, this will only find the first match.
* Aura names are localized, what works in one locale might not work in another.
<syntaxhighlight lang="lua">
/dump AuraUtil.FindAuraByName("Power Word: Fortitude", "player")
</syntaxhighlight>
* Remember to specify the "HARMFUL" filter for debuffs.
<syntaxhighlight lang="lua">
/dump AuraUtil.FindAuraByName("Weakened Soul", "player", "HARMFUL")
</syntaxhighlight>

==Patch changes==
* {{Patch 11.0.2|note=Removed, replaced by {{api|C_UnitAuras.GetAuraDataByIndex}}.}}
* {{Patch 10.2.5|note=Deprecated. Replaced by {{api|t=a|C_UnitAuras.GetAuraDataByIndex}}.}}
* {{Patch 1.14.4|note=Added <code>shouldConsolidate</code> return value.}}
* {{Patch 9.0.1|note=Added <code>MAW</code> filter.<ref>{{ref FrameXML|Blizzard_MawBuffs/Blizzard_MawBuffs.lua|9.0.1|36230|26|2020-10-13}}</ref>}}
* {{Patch 8.0.1|note=Removed querying by name, and removed <code>rank</code> return value.}}
* {{Patch 7.0.3|note=Added <code>nameplateShowAll</code> and <code>timeMod</code>; <code>shouldConsolidate</code> changed to <code>nameplateShowPersonal</code>.}}
* {{Patch 5.1.0|note=<code>isCastByPlayer</code> moved from #17 to #14 after <code>isBossDebuff</code> so that the <code>value[1-n]</code> are at the end and can expand beyond 3 returns.}}
* {{Patch 4.2.0|note=Re-added the return values <code>canApplyAura</code> and <code>isBossDebuff</code>, and added return values <code>value[1-3]</code>.}}
* {{Patch 4.0.1|note=Removed the return values <code>canApplyAura</code> and <code>isBossDebuff</code>.}}
* {{Patch 3.3.0|note=Added <code>shouldConsolidate</code> and <code>spellId</code>.}}
* {{Patch 3.1.0|note=Changed <code>isMine</code> to <code>unitCaster</code>. It is now possible for addons to retrieve the unitId that cast the buff/debuff.}}
* {{Patch 3.0.2|note=Added <code>UnitDebuff()</code> and <code>UnitBuff()</code>}}

==References==
{{Reflist}}

{{apinavbox|UnitAura}}
<!-- luals
---@param unit UnitId
---@param index number
---@param filter? string
---@return string name
---@return number icon
---@return number count
---@return string? dispelType
---@return number duration
---@return number expirationTime
---@return UnitId source
---@return boolean isStealable
---@return boolean nameplateShowPersonal
---@return number spellId
---@return boolean canApplyAura
---@return boolean isBossDebuff
---@return boolean castByPlayer
---@return boolean nameplateShowAll
---@return number timeMod
---@return ...
function UnitAura(unit, index, filter) end

---[Documentation](https://warcraft.wiki.gg/wiki/API_UnitAura)
---@param unit UnitId
---@param index number
---@param filter? string
---@return string name
---@return number icon
---@return number count
---@return string? dispelType
---@return number duration
---@return number expirationTime
---@return UnitId source
---@return boolean isStealable
---@return boolean nameplateShowPersonal
---@return number spellId
---@return boolean canApplyAura
---@return boolean isBossDebuff
---@return boolean castByPlayer
---@return boolean nameplateShowAll
---@return number timeMod
---@return ...
function UnitBuff(unit, index, filter) end

---[Documentation](https://warcraft.wiki.gg/wiki/API_UnitAura)
---@param unit UnitId
---@param index number
---@param filter? string
---@return string name
---@return number icon
---@return number count
---@return string? dispelType
---@return number duration
---@return number expirationTime
---@return UnitId source
---@return boolean isStealable
---@return boolean nameplateShowPersonal
---@return number spellId
---@return boolean canApplyAura
---@return boolean isBossDebuff
---@return boolean castByPlayer
---@return boolean nameplateShowAll
---@return number timeMod
---@return ...
function UnitDebuff(unit, index, filter) end
-->
```