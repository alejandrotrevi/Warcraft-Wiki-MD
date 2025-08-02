# API C Navigation.WasClampedToScreen

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Navigation|system=InGameNavigation}}
Returns true if the navigation frame position was clamped due to having been located off-screen. This can indicate that the player may not be facing towards the tracked location.
 wasClamped = C_Navigation.WasClampedToScreen()

==Returns==
:;wasClamped:{{apitype|boolean}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```