# API IsAdvancedFlyableArea

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Checks if the player is located in a zone that supports advanced flight mechanics, such as [[Dragonriding]].
 flyable = IsAdvancedFlyableArea()

==Returns==
:;flyable:{{apitype|boolean}}

==Details==
* This function corresponds to the <code>advflyable</code> [[Macro conditionals|macro conditional]].
* Contrary to {{api|IsFlyableArea}}, this function returns true in indoor areas where you cannot mount. This can be resolved by additionally querying {{api|IsOutdoors()}}.

==Patch changes==
* {{Patch 10.0.7|note=Added.}}

==See also==
* {{api|IsFlyableArea()}}
```