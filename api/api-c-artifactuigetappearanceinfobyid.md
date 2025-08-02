# API C ArtifactUI.GetAppearanceInfoByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ArtifactUI|system=ArtifactUI}}
Returns information about a selected artifact appearance.
 artifactAppearanceSetID, artifactAppearanceID, appearanceName, displayIndex, unlocked,
  failureDescription, uiCameraID, altHandCameraID, swatchColorR, swatchColorG, swatchColorB,
  modelOpacity, modelSaturation, obtainable
     = C_ArtifactUI.GetAppearanceInfoByID(artifactAppearanceID)

==Arguments==
:;artifactAppearanceID:{{apitype|number}} : [[ArtifactAppearanceID]]

==Returns==
:;1. artifactAppearanceSetID:{{apitype|number}} - The [[setID|appearance set]] this appearance belongs to (from [[API C_ArtifactUI.GetAppearanceSetInfo|C_ArtifactUI.GetAppearanceSetInfo]])
:;2. artifactAppearanceID:{{apitype|number}} : [[ArtifactAppearanceID]]
:;3. appearanceName:{{apitype|string}} - The name of the artifact weapon this appearance goes to
:;4. displayIndex:{{apitype|number}} - The index of this appearance in its set, the same as the appearanceIndex that was entered
:;5. unlocked:{{apitype|boolean}} - Whether this appearance has been unlocked
:;6. failureDescription:{{apitype|string?}} - The requirements for unlocking this appearance. Will return nil for the artifact's base appearance
:;7. uiCameraID:{{apitype|number}}
:;8. altHandCameraID:{{apitype|number?}}
:;9. swatchColorR:{{apitype|number}} - The red component of the appearance swatch button, between 0 and 1
:;10. swatchColorG:{{apitype|number}} - The green component of the appearance swatch button, between 0 and 1
:;11. swatchColorB:{{apitype|number}} - The red component of the appearance swatch button, between 0 and 1
:;12. modelOpacity:{{apitype|number}} - The alpha level (opacity) of the weapon in the Artifact UI, defaulted to 0.5
:;13. modelSaturation:{{apitype|number}} - The saturation level (brightness) of the weapon in the Artifact UI, defaulted to 0.5
:;14. obtainable:{{apitype|boolean}} - Whether the artifact's animation is being suppressed, defaulted to false

==Patch changes==
* {{Patch 8.0.1|note=Added <code>obtainable</code> return.}}
* {{Patch 7.2.0|note=Added.}}

==See also==
* {{api|C_ArtifactUI.GetAppearanceInfo}}()
```