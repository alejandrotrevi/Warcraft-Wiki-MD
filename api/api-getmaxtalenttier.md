# API GetMaxTalentTier

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of available talent tiers.
 tiers = GetMaxTalentTier()

==Returns==
:;tiers:{{apitype|number}} - number of talent tiers available to the player's character, based on the character's level.

==Details==
* Information concerning levels at which talent tiers become available is stored in the <code>CLASS_TALENT_LEVELS</code> global variable, and can be queried like this:
 local _, class = UnitClass("player")
 local tierLevels = CLASS_TALENT_LEVELS[class] or CLASS_TALENT_LEVELS.DEFAULT
 print("Your first talent point is available at level", tierLevels[1]);

==Patch changes==
* {{Patch 5.0.4|note=added}}
```