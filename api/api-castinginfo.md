# API CastingInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the player's currently casting spell.
 name, text, texture, startTime, endTime, isTradeSkill, castID, notInterruptible, spellID = CastingInfo()

==Returns==
:;name:{{apitype|string}} - The name of the spell.
:;text:{{apitype|string}} - The name to be displayed.
:;texture:{{apitype|number}} : [[FileID]]
:;startTime:{{apitype|number}} - Specifies when casting began in milliseconds (corresponds to {{api|GetTime}}()*1000).
:;endTime:{{apitype|number}} - Specifies when casting will end in milliseconds (corresponds to {{api|GetTime}}()*1000).
:;isTradeSkill:{{apitype|boolean}}
:;castID:{{apitype|string}} - e.g. "Cast-3-4479-0-1318-2053-000014AD63"
:;notInterruptible:{{apitype|boolean}} - This is always nil.
:;spellID:{{apitype|number}}

==Details==
* In Classic only casting information for the player is available. This API is essentially the same as {{api|UnitCastingInfo}}("player")</code>

==Patch changes==
* {{Patch 1.13.2|note=Added.}}
```