# API C ArtifactUI.GetArtifactTier

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the tier number for your artifact at the forge.
 tier = C_ArtifactUI.GetArtifactTier()

==Returns==
:;tier:{{apitype|number}} - the '''completed''' tier level of your artifact weapon while at the forge on the Vindicaar.

==Details==
* Returns nil if you are not at the forge or you have no spent tiers.
* If  your weapon is rank 70 as an example, your tier will return 2 even though you might have the first relic at rank 3.

==Patch changes==
* {{Patch 7.3.0|note=Added.}}
```