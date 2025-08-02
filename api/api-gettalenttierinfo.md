# API GetTalentTierInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the column of the selected talent for a given tier.
 tierAvailable, selectedTalent, tierUnlockLevel = GetTalentTierInfo(tier, specGroupIndex [, isInspect, inspectUnit])

==Arguments==
:;tier:{{apitype|number}} - Talent tier from 1 to <code>MAX_TALENT_TIERS</code>
:;specGroupIndex:{{apitype|number}} - Index of active specialization group ({{api|GetActiveSpecGroup}})
:;isInspect:{{apitype|boolean?}} - If non-nil, returns information based on inspectedUnit.
:;inspectUnit:{{apitype|string?}} - Inspected [[unitId]].

==Returns==
:;tierAvailable:{{apitype|boolean}} - true if the player can select a talent for the tier.
:;selectedTalent:{{apitype|number}} - The column number of the selected talent. This is always 0 for inspected units.
:;tierUnlockLevel:{{apitype|number}} - The level the tier becomes available to the player.

==Patch changes==
* {{Patch 9.0.1|note=Added <code>tierUnlockLevel</code> return, which replaced <code>CLASS_TALENT_LEVELS</code> usage.}}
```