# API C ArtifactUI.GetArtifactInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the currently equipped artifact weapon.
 itemID, altItemID, name, icon, xp, pointsSpent, quality, artifactAppearanceID, appearanceModID, itemAppearanceID, altItemAppearanceID, altOnTop, tier = C_ArtifactUI.GetArtifactInfo()

==Returns==
:;1. itemID:{{apitype|number}} - Numeric ID of the main-hand weapon
:;2. altItemID:{{apitype|number?}} - Numeric ID of the off-hand weapon, or nil if there is none
:;3. name:{{apitype|string}} - Name of the weapon
:;4. icon:{{apitype|fileID}} - The fileID for the icon texture for the artifact
:;5. xp:{{apitype|number}} - The artifact power available to this weapon
:;6. pointsSpent:{{apitype|number}} - The number of ranks that have been purchased (not granted by relics)
:;7. quality:{{apitype|number}}
:;8. artifactAppearanceID:{{apitype|number}} - The currently active artifact appearanceID
:;9. appearanceModID:{{apitype|number}}
:;10. itemAppearanceID:{{apitype|number?}} - The transmogrification appearanceID used on the main-hand weapon
:;11. altItemAppearanceID:{{apitype|number?}} - The transmogrification appearanceID used on the off-hand weapon
:;12. altOnTop:{{apitype|boolean}} - Whether the off-hand item is displayed
:;13. tier:{{apitype|ArtifactTiers}}

==Details==
*Values 3 and 11 only apply to artifacts that provide both a main-hand and an off-hand item (such as [[Felo'melorn]]).  Artifacts that are two-handed (with the exception of [[Odyn's Fury]] and [[Helya's Wrath]]) will return these values as 'nil'.
*Values 10 and 11 will return 'nil' if no transmog has been applied to their corresponding items.
*Values 3 through 7 are not explicitly named anywhere in Blizzard's API; their names are assumed based on their function

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```