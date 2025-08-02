# API C AnimaDiversion.GetOriginPosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AnimaDiversion|system=AnimaDiversionInfo}}
Locates an [[Anima Conductor]].
 normalizedPosition = C_AnimaDiversion.GetOriginPosition()

==Returns==
:;normalizedPosition:{{apitype|vector2}} - An Anima Conductor's location on the continent map only while interacting with it; otherwise nil.

==Details==
* This function begins returning information once the player clicks on an Anima Conductor, but stops once the player is no longer in range to interact with it further.

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```