# API GetActiveArtifactByRace

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the active Archaeology artifact for a race.
 artifactName, artifactDescription, artifactRarity, artifactIcon, hoverDescription, keystoneCount, bgTexture = GetActiveArtifactByRace(branchIndex, artifactIndex)

==Arguments==
:;branchIndex:{{apitype|number}} - Index of the race to pick the artifact from.
:;artifactIndex:{{apitype|number}}

==Returns==
:;artifactName:{{apitype|string}} - The name of the artifact.
:;artifactDescription:{{apitype|string}} - The description displayed on the artifact detail page. Only visible after completion for rare artifacts.
:;artifactRarity:{{apitype|string}} - The rarity of the artifact, 0 for Common and 1 for Rare.
:;artifactIcon:{{apitype|string}} - The path to the artifact's icon texture.
:;hoverDescription:{{apitype|string}} - The description shown in the tooltip when hovering over the completed artifact. Not visible before the artifact is completed. Not readily available on function call, see [[SpellMixin#ContinueOnSpellLoad|SpellMixin:ContinueOnSpellLoad]].<ref name="BFA" />
:;keystoneCount:{{apitype|number}} - The number of [[Keystone]] slots this artifact has. Only visible when this is the in progress artifact.
:;bgTexture:{{apitype|string}} - The path to the artifact's background texture. Only displayed when the artifact is rare.

==Patch changes==
* {{Patch 8.0.1|note=Fifth return value is only available after information loads on demand.<ref name="BFA">[https://us.battle.net/forums/en/wow/topic/20762318007 ''Battle for Azeroth Addon Changes''] forum [[blue post]] by [[Ythisens]], 24 Apr 2018</ref>}}
* {{Patch 4.0.1|note=Added.}}

==See also==
: {{api|GetArtifactInfoByRace}}(raceIndex, artifactIndex)
: {{api|GetSelectedArtifactInfo}}()

==References==
<references />
```