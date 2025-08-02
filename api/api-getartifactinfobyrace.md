# API GetArtifactInfoByRace

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the information for a specific race's artifact.
 artifactName, artifactDescription, artifactRarity, artifactIcon, hoverDescription, keystoneCount, bgTexture, firstCompletionTime, completionCount = GetArtifactInfoByRace(raceIndex, artifactIndex)

==Arguments==
:;raceIndex:{{apitype|number}} - Index of the race to pick the artifact from.
:;artifactIndex:{{apitype|number}} - Index of the artifact.

==Returns==
:;artifactName:{{apitype|string}} - The name of the artifact.
:;artifactDescription:{{apitype|string}} - The description displayed on the artifact detail page. Only visible after completion for rare artifacts.
:;artifactRarity:{{apitype|number}} - The rarity of the artifact, 0 for Common and 1 for Rare.
:;artifactIcon:{{apitype|string}} - The path to the artifact's icon texture.
:;hoverDescription:{{apitype|string}} - The description shown in the tooltip when hovering over the completed artifact. Not visible before the artifact is completed. Not readily available on function call, see [[SpellMixin#ContinueOnSpellLoad|SpellMixin:ContinueOnSpellLoad]].
:;keystoneCount:{{apitype|number}} - The number of [[Keystone]] slots this artifact has. Only visible when this is the in progress artifact.
:;bgTexture:{{apitype|string}} - The path to the artifact's background texture. Only displayed when the artifact is rare.
:;firstCompletionTime:{{apitype|number}} - The first time the artifact was ever completed, in the same format as time().
:;completionCount:{{apitype|number}} - The number of times this artifact has been completed.

==Details==
: Rare artifacts are always at the front of the list of completed artifacts. For example, if you have two rare artifacts, their indices will always be 2 and 3.
: The formatting used in the US client for the display of the firstCompletionTime tooltip is "%m/%d/%y %I:%M %p". You can view this formatting using the date() function and the firstCompletionTime.

==Example==
The snippet below prints number of completed artifacts for the every Archaeology race.
 /run print("Total artifacts"); for x=1,9 do local c=GetNumArtifactsByRace(x); local a =0; for y=1,c do local t = select(9, GetArtifactInfoByRace(x, y)); a=a+t;end local rn = GetArchaeologyRaceInfo(x); if( c > 1 ) then print(rn .. ": " .. a); end end

==Patch changes==
* {{Patch 4.0.6|note=Behavior changed|comment=As of patch 4.0.6, the artifact in progress for the race is no longer necessarily index 1, if the artifact is not solved for the first time. For this functionality see [[API GetActiveArtifactByRace|GetActiveArtifactByRace]].}}
* {{Patch 4.0.1|note=Added.}}
```