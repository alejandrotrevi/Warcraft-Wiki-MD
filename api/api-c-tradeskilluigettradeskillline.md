# API C TradeSkillUI.GetTradeSkillLine

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the current profession displayed in the trade skill window.
 skillLineID, skillLineDisplayName, skillLineRank, skillLineMaxRank, skillLineModifier, parentSkillLineID, parentSkillLineDisplayName = C_TradeSkillUI.GetTradeSkillLine()

==Returns==
:;skillLineID:{{apitype|number}} - [[TradeSkillLineID]].
:;skillLineDisplayName:{{apitype|string}} - Localized name.
:;skillLineRank:{{apitype|number}} - Current skill level.
:;skillLineMaxRank:{{apitype|number}} - Maximum attainable skill level.
:;skillLineModifier:{{apitype|number}} - Modifiers to the skill level (such as +mining, +cooking, etc).
:;parentSkillLineID:{{apitype|number}} - [[TradeSkillLineID]] of the parent tradeskill (i.e. Alchemy if this skill is Legion Alchemy)
:;parentSkillLineDisplayName:{{apitype|string?}} - Localized name of the parent tradeskill.

==Patch changes==
* {{Patch 8.0.1|note=Added <code>parentSkillLineID, parentSkillLineDisplayName</code> arguments.<ref>{{Ref FrameXML|Blizzard_TradeSkillUI/Blizzard_TradeSkillUI.lua|8.0.1|27101|110|2018-07-16}}</ref>}}
* {{Patch 7.0.3|note=Changed to <code>C_TradeSkillUI.GetTradeSkillLine()</code>. Added <code>skillLineID</code> argument. Returns nil if the frame is closed.<ref>{{Ref FrameXML|Blizzard_TradeSkillUI/Blizzard_TradeSkillUI.lua|7.0.3|22594|110|2016-09-08}}</ref>|
comment=Previously returned "UNKNOWN" when the frame was closed}}
* {{Patch 4.0.3|note=Added <code>skillLineModifier</code> argument.<ref>{{Ref FrameXML|Blizzard_TradeSkillUI/Blizzard_TradeSkillUI.lua|4.0.3|13329|425|2010-10-19}}</ref>}}
* {{Patch 1.8.0|note=Added as <code>name, rank, maxRank = GetTradeSkillLine()</code><ref>{{Ref FrameXML|Blizzard_TradeSkillUI/Blizzard_TradeSkillUI.lua|1.8.0|4735|174|2005-10-11}}</ref>}}

==References==
{{Reflist}}
```