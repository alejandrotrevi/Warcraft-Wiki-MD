# API UnitCastingInfo

**Contributor:** Cosmic Cleric

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns information about the spell currently being cast by the specified unit.
 name, text, texture, startTimeMS, endTimeMS, isTradeSkill, castID, notInterruptible, spellId = UnitCastingInfo(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;name:{{apitype|string}} - The name of the spell, or nil if no spell is being cast.
:;text:{{apitype|string}} - The name to be displayed.
:;texture:{{apitype|string}} - The texture path associated with the spell icon.
:;startTimeMS:{{apitype|number}} - Specifies when casting began in milliseconds (corresponds to [[API GetTime|GetTime()]]*1000).
:;endTimeMS:{{apitype|number}} - Specifies when casting will end in milliseconds (corresponds to [[API GetTime|GetTime()]]*1000).
:;isTradeSkill:{{apitype|boolean}} - Specifies if the cast is a tradeskill
:;castID:{{apitype|string}} : [[GUID#Cast|GUID]] - The unique identifier for this spell cast, for example <code>Cast-3-3890-1159-21205-8936-00014B7E7F</code>.
:;notInterruptible:{{apitype|boolean}} - if true, indicates that this cast cannot be interrupted with abilities like [[Kick]] or [[Pummel]]. In default UI those spells have shield frame around their icons on enemy cast bars. Always returns <code>nil</code> in Classic {{bc-inline}}.
:;spellId:{{apitype|number}} - The spell's unique identifier. (Added in 7.2.5)

==Details==
* For channeled spells, displayName is "Channeling". So far displayName is observed to be the same as name in any other contexts.
* This function may not return anything when the target is channeling spell post it warm-up period, you should use {{api|UnitChannelInfo}}  in that case. It takes the same arguments and returns similar values specific to channeling spells. Be careful, that although similar, it has different amount of returns and different positions for some returns.
* {{wow-inline}} In Classic, the alternative {{api|CastingInfo}}() is similar to <code>UnitCastingInfo("player")</code>
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|UNIT_SPELLCAST_START}}<br>{{api|t=e|UNIT_SPELLCAST_STOP}} }}
{{apirow | Related API | {{api|CastingInfo}} (Classic)}}
|}

==Example==
The following snippet prints the amount of time remaining before the player's current spell finishes casting.
<syntaxhighlight lang="lua">
local spell, _, _, _, endTimeMS = UnitCastingInfo("player")
if spell then 
    local finish = endTimeMS/1000 - GetTime()
    print(spell .. " will be finished casting in " .. finish .. " seconds.")
end
</syntaxhighlight>

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 8.0.1|note=Removed the second parameter, "nameSubtext". Second parameter is now "text" (former third parameter).}}
* {{Patch 7.2.5|note=The castID return value is now a [[GUID]]. Previously it represented the number of spell casts since the game was started.}}
* {{Patch 2.0.1|note=Added.<ref>{{ref web|author={{Blizz}}[[slouken]]|date=20061006|url=http://forums.worldofwarcraft.com/thread.html?topicId=15401595&pageNo=8&sid=1#146|archiveurl=http://blue.cardplace.com/newcache/us/15401595.htm|title=Re: Expansion Changes - Concise List}}</ref>}}
====<font color="#4ec9b0">Classic</font>====
* {{Patch 2.5.3|note=Added <code>notInterruptible</code> (nil) for api consistency.}}

==References==
{{reflist}}
```