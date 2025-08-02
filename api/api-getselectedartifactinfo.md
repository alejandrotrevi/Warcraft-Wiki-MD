# API GetSelectedArtifactInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the selected race's Archaeology artifact.
 artifactName, artifactDescription, artifactRarity, artifactIcon, hoverDescription, keystoneCount, bgTexture, spellID = GetSelectedArtifactInfo()

==Returns==
:;1. artifactName:{{apitype|string}} - The name of the archaeology artifact being reconstructed.
:;2. artifactDescription:{{apitype|string}} - The description displayed on the artifact detail page. Only visible after completion for rare artifacts.
:;3. artifactRarity:{{apitype|number}} - The rarity of the artifact, 0 for Common and 1 for Rare.
:;4. artifactIcon:{{apitype|number}} ([[fileID]]) - The artifact's icon texture.
:;5. hoverDescription:{{apitype|string}} - The description shown in the tooltip when hovering over the completed artifact. Not visible before the artifact is completed. Not readily available on function call, see [[SpellMixin#ContinueOnSpellLoad|SpellMixin:ContinueOnSpellLoad]].
:;6. keystoneCount:{{apitype|number}} - The number of [[Keystone]] slots this artifact has.
:;7. bgTexture:{{apitype|number}} ([[fileID]]) - The artifact's background texture.
:;8. spellID:{{apitype|number}} - The ID of the spell cast when solving the artifact.

==Patch changes==
* {{Patch 8.0.1|note=Removed <code>firstCompletionTime, completionCount</code> return values (still available through {{api|GetArtifactInfoByRace}}).}}
* {{Patch 7.3.0|note=artifactIcon and bgTexture return values changed from a string texture paths to [[fileID]]s.}}
* {{Patch 4.0.1|note=Added.}}

==See Also==
* [[API SetSelectedArtifact|SetSelectedArtifact]]
* [[API GetActiveArtifactByRace|GetActiveArtifactByRace]]
* [[API GetArtifactInfoByRace|GetArtifactInfoByRace]]
```