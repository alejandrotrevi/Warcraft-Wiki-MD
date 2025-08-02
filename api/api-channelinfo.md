# API ChannelInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the player's currently channeling spell.
 name, text, texture, startTime, endTime, isTradeSkill, notInterruptible, spellID = ChannelInfo()

==Returns==
:;name:{{apitype|string}} - The name of the spell, or nil if no spell is being channeled.
:;text:{{apitype|string}} - The name to be displayed.
:;texture:{{apitype|number}} : [[FileID]]
:;startTime:{{apitype|number}} - Specifies when channeling began in milliseconds (corresponds to {{api|GetTime}}()*1000).
:;endTime:{{apitype|number}} - Specifies when channeling will end in milliseconds (corresponds to {{api|GetTime}}()*1000).
:;isTradeSkill:{{apitype|boolean}}
:;notInterruptible:{{apitype|boolean}} - This is always nil.
:;spellID:{{apitype|number}}

==Details==
* In Classic only channeling information for the player is available. This API is essentially the same as {{api|UnitChannelInfo}}("player")</code>

==Patch changes==
* {{Patch 1.13.2|note=Added.}}
```