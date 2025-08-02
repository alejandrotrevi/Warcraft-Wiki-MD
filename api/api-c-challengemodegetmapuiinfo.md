# API C ChallengeMode.GetMapUIInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 name, id, timeLimit, texture, backgroundTexture, mapID = C_ChallengeMode.GetMapUIInfo(mapChallengeModeID)

==Arguments==
:;mapChallengeModeID:{{apitype|number}} : {{dbc|mapchallengemode|MapChallengeMode.ID}}

==Returns==
:;name:{{apitype|string}}
:;id:{{apitype|number}} : MapChallengeMode.ID
:;timeLimit:{{apitype|number}} - The time limit in seconds.
:;texture:{{apitype|number?}} : [[FileID]]
:;backgroundTexture:{{apitype|number}} : [[FileID]]
:;mapID:{{apitype|number}}

==Patch changes==
* {{Patch 11.2.0|note=Added <code>mapID</code> return value.}}
* {{Patch 8.0.1|note=Added.}}
```