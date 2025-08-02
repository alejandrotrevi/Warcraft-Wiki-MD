# API C AnimaDiversion.GetTextureKit

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AnimaDiversion|system=AnimaDiversionInfo}}
Names the texture kit applied to the AnimaDiversionFrame.
 textureKit = C_AnimaDiversion.GetTextureKit()

==Returns==
:;textureKit:{{apitype|string?}} - Name of a texture kit if the player has interacted with an Anima Conductor at least once since logging on; otherwise, returns nil.

==See also==
* {{api|t=e|ANIMA_DIVERSION_OPEN}} - The payload contains the textureKit.

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```