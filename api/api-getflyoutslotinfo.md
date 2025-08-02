# API GetFlyoutSlotInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Describes an action bar flyout slot.
 flyoutSpellID, overrideSpellID, isKnown, spellName, slotSpecID = GetFlyoutSlotInfo(flyoutID, slot)

==Arguments==
:;flyoutID:{{apitype|number}} - The second return value of {{api|GetSpellBookItemInfo}}() or {{api|GetActionInfo}}().
:;slot:{{apitype|number}}

==Returns==
:;flyoutSpellID:{{apitype|number}}
:;overrideSpellID:{{apitype|number}}
:;isKnown:{{apitype|boolean}}
:;spellName:{{apitype|string}}
:;slotSpecID:{{apitype|number}}

==Details==
* The in-game error handler erroneously describes only two return values when there are at least five.

==Patch changes==
* {{Patch 5.0.4|note=Several return values added.<ref>{{ref FrameXML|SpellBookFrame.lua|5.0.4|16016|148|2012-08-21}}</ref>}}
* {{Patch 4.0.1|note=Added.}}

==References==
{{Reflist}}
```