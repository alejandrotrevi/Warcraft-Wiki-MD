# API C Navigation.HasValidScreenPosition

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Navigation|system=InGameNavigation}}
Returns true if the currently tracked location can be represented by any screen position. This can presumably return false a tracked location weren't valid for the current map, or if the player is possibly too close to a tracked location.
 hasValidScreenPosition = C_Navigation.HasValidScreenPosition()

==Returns==
:;hasValidScreenPosition:{{apitype|boolean}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```