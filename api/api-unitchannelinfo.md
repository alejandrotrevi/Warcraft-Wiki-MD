# API UnitChannelInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns information about the spell currently being channeled by the specified unit.
 name, displayName, textureID, startTimeMs, endTimeMs, isTradeskill, notInterruptible, spellID, isEmpowered, numEmpowerStages = UnitChannelInfo(unitToken)

==Arguments==
:;unitToken:{{apitype|string}} : [[UnitId]]

==Returns==
:;name:{{apitype|string}} - The name of the spell, or nil if no spell is being channeled.
:;displayName:{{apitype|string}} - The name to be displayed.
:;textureID:{{apitype|string}} - The texture path associated with the spell icon.
:;startTimeMs:{{apitype|number}} - Specifies when channeling began, in milliseconds (corresponds to [[API GetTime|GetTime()]]*1000).
:;endTimeMs:{{apitype|number}} - Specifies when channeling will end, in in milliseconds (corresponds to [[API GetTime|GetTime()]]*1000).
:;isTradeskill:{{apitype|boolean}} - Specifies if the cast is a tradeskill.
:;notInterruptible:{{apitype|boolean}} - if true, indicates that this channeling cannot be interrupted with abilities like [[Kick]] or [[Pummel]]. In default UI those spells have shield frame around their icons on enemy channeling bars. Always returns <code>nil</code> in Classic {{bc-inline}}.
:;spellID:{{apitype|number}} - The spell's unique identifier.
:;isEmpowered:{{apitype|boolean}}
:;numEmpowerStages:{{apitype|number}}

==Details==
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|UNIT_SPELLCAST_CHANNEL_START}}<br>{{api|t=e|UNIT_SPELLCAST_CHANNEL_STOP}} }}
{{apirow | Related API | {{api|ChannelInfo}} (Classic)}}
|}

==Example==
The following snippet prints the amount of time remaining before the player's current spell finishes channeling.
 local spell, _, _, _, endTimeMS = UnitChannelInfo("player")
 if spell then 
  local finish = endTimeMS/1000 - GetTime()
  print(spell .. ' will be finished channeling in ' .. finish .. ' seconds.')
 end

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 8.0.1|note=Removed the second parameter, "nameSubtext". Second parameter is now "text" (former third parameter).}}
* {{Patch 2.0.1|note=Added.<ref>{{ref web|author={{Blizz}}[[slouken]]|date=20061006|url=http://forums.worldofwarcraft.com/thread.html?topicId=15401595&pageNo=8&sid=1#146|archiveurl=http://blue.cardplace.com/newcache/us/15401595.htm|title=Re: Expansion Changes - Concise List}}</ref>}}
====<font color="#4ec9b0">Classic</font>====
* {{Patch 2.5.3|note=Added <code>notInterruptible</code> (nil) for api consistency.}}

==References==
```