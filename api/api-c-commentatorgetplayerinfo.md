# API C Commentator.GetPlayerInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 unitToken, name, faction, specialization, damageDone, damageTaken, healingDone, healingTaken, kills, deaths = C_Commentator.GetPlayerInfo(teamIndex, playerIndex)

==Arguments==
:;teamIndex:{{apitype|number}}
:;playerIndex:{{apitype|number}}

==Returns==
:;unitToken:{{apitype|string}} : [[UnitId]]
:;name:{{apitype|string}}
:;faction:{{apitype|number}}
:;specialization:{{apitype|number}}
:;damageDone:{{apitype|number}}
:;damageTaken:{{apitype|number}}
:;healingDone:{{apitype|number}}
:;healingTaken:{{apitype|number}}
:;kills:{{apitype|number}}
:;deaths:{{apitype|number}}

==Patch changes==
* {{Patch 6.1.0|note=Added.}}
```