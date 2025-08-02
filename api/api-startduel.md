# API StartDuel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Challenges the specified player to a duel.
 StartDuel(unit)
 StartDuel(name [, exactMatch])

==Arguments==
{{:UnitArg}}

==Details==
* <code>StartDuel("player")</code> is an apparent special case, creating a mouse cursor to select someone else to duel against.

==Patch changes==
<!-- * {{Patch 2.0.4|note=Unprotected.}} --> <!-- Probably the right patch. -->
<!-- * {{Patch 2.0.1|note=<code>StartDuel()</code> now has two forms, replacing <code>StartDuelUnit()</code>.<ref>{{ref FrameXML|UnitPopup.lua|2.0.1|6180|636|2006-12-05}}</ref>  Both forms are protected.|comment=}} -->
* {{Patch 1.0.0|note=Added <code>StartDuel()</code><ref>{{ref FrameXML|ChatFrame.lua|1.1.2|4115|999|2004-12-06}}</ref> and <code>StartDuelUnit()</code><ref>{{ref FrameXML|UnitPopup.lua|1.1.2|4115|352|2004-12-06}}</ref>.}}

==See also==
* {{api|AcceptDuel()}}
* {{api|CancelDuel()}}

==References==
{{Reflist}}
<!-- luals
---@param unit string
---@overload fun(name: string, exactMatch?: boolean)
function StartDuel(unit) end
-->
```