# API C ArtifactUI.GetAppearanceInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ArtifactUI|system=ArtifactUI}}
Returns information about a selected artifact appearance.
 artifactAppearanceID, appearanceName, displayIndex, unlocked, failureDescription,
  uiCameraID, altHandCameraID, swatchColorR, swatchColorG, swatchColorB, modelOpacity,
  modelSaturation, obtainable
     = C_ArtifactUI.GetAppearanceInfo(appearanceSetIndex, appearanceIndex)

==Arguments==
:;appearanceSetIndex:{{apitype|number}} - Ranging from 1 to {{api|C_ArtifactUI.GetNumAppearanceSets}}()
:;appearanceIndex:{{apitype|number}} - Numeric index of the appearance in the specified setIndex, from 1 to 4 -- '''exception:''' Set 1 for both the Feral and the Guardian Druid Artifacts, which has 7 appearances total, due to racial basic tints: Troll/Zandalari is tint 1, Tauren/Highmountain is tint 2, Night Elf is tint 3, Worgen/Kul Tiran is tint 4, and 5 to 7 for the Pillar of Creation, Light's Heart, and Campaign Effort criteria that would otherwise be index 2 to 4. Querying racial tints other than the one for the current character's race returns nil.

==Returns==
:;1. artifactAppearanceID:{{apitype|number}} : [[ArtifactAppearanceID]]
:;2. appearanceName:{{apitype|string}} - The name of the artifact weapon this appearance goes to
:;3. displayIndex:{{apitype|number}} - The index of this appearance in its set, the same as the appearanceIndex that was entered
:;4. unlocked:{{apitype|boolean}} - Whether this appearance has been unlocked
:;5. failureDescription:{{apitype|string?}} - The requirements for unlocking this appearance. Will return nil for the artifact's base appearance
:;6. uiCameraID:{{apitype|number}}
:;7. altHandCameraID:{{apitype|number?}}
:;8. swatchColorR:{{apitype|number}} - The red component of the appearance swatch button, between 0 and 1
:;9. swatchColorG:{{apitype|number}} - The green component of the appearance swatch button, between 0 and 1
:;10. swatchColorB:{{apitype|number}} - The red component of the appearance swatch button, between 0 and 1
:;11. modelOpacity:{{apitype|number}} - The alpha level (opacity) of the weapon in the Artifact UI, defaulted to 0.5
:;12. modelSaturation:{{apitype|number}} - The saturation level (brightness) of the weapon in the Artifact UI, defaulted to 0.5
:;13. obtainable:{{apitype|boolean}} - Whether the artifact's animation is being suppressed, defaulted to false

==Patch changes==
* {{Patch 8.0.1|note=Added <code>obtainable</code> return.}}
* {{Patch 7.0.3|note=Added.}}
```