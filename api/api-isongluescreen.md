# API IsOnGlueScreen

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Glue}} {{deprecatedapi|patch=11.0.5}}
Returns whether the game is currently showing a GlueXML screen (i.e. no character is logged in).
 isOnGlueScreen = IsOnGlueScreen()

==Returns==
:;isOnGlueScreen:{{apitype|boolean}} - false if a character is logged in; true otherwise.

==Details==
* This function will always return false if called by an AddOn -- addons only run when a character is logged in.

==Patch changes==
* {{Patch 11.0.5|note=Removed. Note that due to a bug, the IsOnGlueScreen global is assigned a boolean value<ref>https://github.com/Gethe/wow-ui-source/blob/11.0.5/Interface/AddOns/Blizzard_DeprecatedGlue/Deprecated_Glue.lua#L9</ref> and does not alias to the replacement function.}}
* {{Patch 5.4.2|note=Added.}}

==References==
```