# API C AddOns.EnableAllAddOns

**Contributor:** Ghostopheles

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AddOns|system=AddOns}}
Sets all addons to be enabled.
 C_AddOns.EnableAllAddOns([character])

==Arguments==
:;character:{{apitype|string?}} - The name or [[GUID]] of the character, excluding the realm name. If omitted, enables all addons for all characters.

==Details==
: All addons will be enabled on the next session, when reloading or relogging.
```