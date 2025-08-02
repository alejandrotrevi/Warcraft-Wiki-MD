# API IsFlyableArea

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns true if the current zone is a flyable area.
 flyable = IsFlyableArea()

==Returns==
:;flyable:{{apitype|boolean}}

==Details==
* This function corresponds to the <code>flyable</code> [[Macro conditionals|macro conditional]].
* This function will return false if the player is located in an {{api|IsIndoors|indoors}} area where mounts typically cannot be used.

==Patch changes==
* {{Patch 2.1.0|note=Added.}}

==See also==
* {{api|IsAdvancedFlyableArea()}}
```