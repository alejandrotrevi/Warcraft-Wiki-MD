# API C Garrison.GetFollowerAutoCombatSpells

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Garrison|system=GarrisonInfo}}
Needs summary.
 autoCombatSpells, autoCombatAutoAttack = C_Garrison.GetFollowerAutoCombatSpells(garrFollowerID, followerLevel)

==Arguments==
:;garrFollowerID:{{apitype|string}}
:;followerLevel:{{apitype|number}}

==Returns==
:;autoCombatSpells:{{apitype|AutoCombatSpellInfo[]}}
:;autoCombatAutoAttack:{{apitype|AutoCombatSpellInfo?}}
{{:Struct AutoCombatSpellInfo|nocaption=1}}

==Patch changes==
* {{Patch 9.1.0|note=Added <code>autoCombatAutoAttack</code> return.}}
* {{Patch 9.0.1|note=Added.}}
```