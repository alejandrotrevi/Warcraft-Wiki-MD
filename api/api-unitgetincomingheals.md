# API UnitGetIncomingHeals

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the predicted heals cast on the specified unit.
 heal = UnitGetIncomingHeals(unit [, healerGUID])

==Arguments==
:;unit:{{apitype|UnitToken}}
:;healerGUID:{{apitype|UnitToken?}} - Only predict incoming heals from a single [[UnitId]].

==Returns==
:;heal:{{apitype|number}} - Predicted increase in health from incoming heals.

==Details==
* {{bc-inline}} For Classic, this function is only partially functional<ref>https://github.com/Stanzilla/WoWUIBugs/issues/163</ref>. The returned value only predicts healing from direct spell casts; heal-over-time effects and channelled casts are not factored into any predictions.

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 4.0.1|note=Added.<ref>{{ref FrameXML|CompactUnitFrame.lua|4.0.1|13164|425|20101019}}</ref>}}

====<font color="#4ec9b0">Classic</font>====
* {{Patch 1.14.0|note=Backported from [[patch 2.5.2]].}}
* {{Patch 2.5.2|note=Added, excluding heals over time.}}

==See Also==
* {{api|UnitHealth}}
* {{api|UnitHealthMax}}
* {{api|UnitGetTotalAbsorbs}}

==References==
{{reflist}}
```