# API GetCorruptionResistance

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Tracks how much the player has offset their exposure to dangers that result from wearing items touched by [[N'Zoth]]'s influence.
 corruptionResistance = GetCorruptionResistance()

==Returns==
:;corruptionResistance:{{apitype|number}} - Amount of corruption resistance, independent of how much corruption is actually present

==Example==
 local c, r = GetCorruption(), GetCorruptionResistance()
 print("You have " .. max(0, c - r) .. " net corruption")  -- max to prevent negative values

==Patch changes==
* {{Patch 8.3.0|note=Added.}}

==See also==
* {{api|GetCorruption}}()
```